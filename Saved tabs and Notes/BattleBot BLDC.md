- For choosing motors of different kV... un motors ko calculator mein daalke dekho ki different gear ratios aur volatage mein changes karke kya effect hoga, and heat output dekhna ho then Resitance pata hogi motors ki to unse calculate kar lena ki relatively difference kya hoga.

- Check if true actually - Higer Kv have lower max Voltage, which is ideal as in our case we are doing 6S which is typically the lowest Max Voltage for BLDCs, thought is that we can churn the most power for the Voltage(i.e. 24 in our case). How does this affect the other characteristics of the motor, surely there should be implications? Check [Vedder article](https://vedder.se/2014/10/chosing-the-right-bldc-motor-and-battery-setup-for-an-electric-skateboard/) for choosing skateboard motors. Agar motor is rated for a higher Voltage than what we are running on, does this mean that the motor just got more inefficient? Since heat loss is I^2R, and it would be same irrespective of Voltage??(Think in terms of resistance, as Resistance squared hota for difference between motors of same dimension but different kv i.e. different max voltage)

- BLDC ki max speed (unloaded) tab hoti jab back emf is equal to supply voltage. Torque is prop to amount of current flowing. At no load max speed, no diff in voltage b/w voltage of motor and supply, hence no current, hence no torque.\
Torque is thermally contrained. This thermally constrained torque is rated torque. Max speed at which motor can operate forever at its rated torque is base speed.\
OR THe base speed (also called the rated or nominal speed) is the top speed at which a brushless motor can achieve at it's 'rated torque'. The 'rated torque' is the torque that a motor can output indefinitely without overheating.\
As a rule of thumb, the rated current, and therefore torque output, of a hobbyist motor will be around one third that of the peak torque value, or around two thirds with aggressive forced air cooling.\
The best way to keep your motor cool is to use a motor big enough to handle the load, run it at the highest voltage you can (usually 12s) and gear it appropriately so that your target top speed is ~80% of your esc's max erpm.

---

## ESC
- Should we consider whether tuning of ESC is available or not?
- https://spintend.com/ - best quality to price for VESC
- Are the normal drone esc okay be used for our case, checkup SimonK and how its tuned
- Tekin
- Maytech
- Flipsky 75100 or 75200 or 75300 or 75350 (Overkill)

- The magnetic strength is proportional to the amount of current in the coils

- https://www.reddit.com/r/Nerf/comments/72ybn9/high_fps_flywheels_and_brushless_motors_a/
the most important of which is the coil resistance, in the case of the Multistar Elite 2204-2300kv it is 0.125 ohms. This would suggest, despite an 11.5 amp rating, a stall current of ~96amps, and so an extraordinary stall torque of 4,066g.cm… but it’s not quite that simple. \
Before we can assess the FDL we need to understand a little bit about how brushless motors are controlled. The SymonK firmware on the ESC does something interesting. The speed controller does not know what the current is going through it so it does a basic form of current limiting to protect itself and the motor. By default, when the motor start the firmware limits it to a 25% duty cycle, limiting the motor to 25% voltage, meaning the current when it start is reduced to 1,016g.cm. However, the controller then begins to ramp up the voltage applied as the motor accelerates until it reaches an RPM determined by a preset speed, which for this motor and standard firmware is 1627 RPM. What this means is that when the motor reaches 1627 RPM and the full voltage is applied, the torque has increased to 3,824g.cm. Now that is a big number, but there are other factors to consider.

## From AskAaron
- BLDC ki weight roughly 4.4 - 5.1 % of robot weight. (For 8 Kg 4.8% = ~400g)
- At the least 60 joules per kg; 60x8 = 480J. This is the minimum energy that it should store, but would be better we three times of that.
- For spin-up time -  aim to spin your weapon up to at least 45 joules per kilo of the bot's weight class in the first two seconds  
Peak power output is available when the load on the motor limits speed to 1/2 the unloaded motor RPM.  
Peak Output Watts = Voltage^2 ÷ Resistance × 0.25  
Stall Amperage = Voltage ÷ Terminal Resistance

- The problem is that the faster the weapon spins, the harder it is to get the weapon to 'bite' into your opponent and get a powerful hit. Atleast the bite of 7mm
Useable Impactor Height = (Attack speed [in units per second] × 60) ÷ (Weapon RPM × Number of Impactors)



## Weapon Motor

- Agar BLDC to ESC kaise choose kare - current rating se. BLDC ki windings ki current sehne ki limitation hoti, and ek Voltage ki.
- Weapon Drum ki MOI pata lag jaaye, to usse time to reach full speed, or even just ki wo equation kya hogi?
- Kya load mein BLDC even apne highest power tak pahuch paati

---

