- Replace RS775 with BLDC while keeping the same gearbox. Check curves for BLDC about speed and torque and power to see if its viable
- Voltage double pe rpm double? Basically check the curves for BLDC while varying voltage
- Brushed esc ki rating kaise dekhte jab voltage double ho jaata, like since rpm double ho rahi, current utna hi rahega kya?(all while Power double ho rahi) and kya esc ki Watt limitation hoti? ki bas current limitation hoti jisse power limitation aati (Power = V * I )?
- Nayi ESC ka budget hai? and nayi 24V battery(ies) ka? motor to sahi hai RS7775 waali, and RPM bhi agar 24V pe chala rahe, and current bhi typically utna jyaada hoga nahi as Stall current 30A hai, rated current kuch 13A hi hai.

- Would cytron motor drivers work?

- For the current 1625 esc, how to check if the motor has stopped or not? Use this a feedback to continuously send signal to change direction until it actually starts moving in the direction we want

- For new motor controller, to check if motors moving in sync?(i.e. straight chal rahe?

# Driving Soln
Servo.h to feed signal to esc. Continuously send signals to the esc to for reversing, and stop when you get a positive signal from the ouput wire of the esc. Research on what effects will adding diodes have on the current drive esc.
You may implement a way to stop that continuous reverse signal, by checking if the motor has stopped by other means.


Or exclude this alltogether and implement a system of non reversible turning, i.e. if throttle is more than 1500 then none of the motors should reverse even when turning, and vice versa.
Potential issue that the turning would be very slow.
---
## Drive
- Replace RS775 with BLDC while keeping the same gearbox. Jyaada current ki esc ki jaroorat nahi, just reversible esc honi chahiye.
- Voltage double
- Cytron ki nayi ESC's kaam karengi? phookengi to nahi, due to inductance and what not...?
