# Resources
- Check the sources from the Gemini Chats
- Check the main folder for guides
- Check the saved tabs
- Review the YouTube playlist
- Saved Reddit comments/Posts

---

Essential Resources for Learning and Inspiration
To effectively prepare for this project, your team should leverage the wealth of resources available within the combat robotics community.

Online Forums and Communities: Engaging with online forums and communities is an invaluable way to learn from experienced battlebot builders, ask specific questions, and gain insights from their project logs. Platforms like Reddit's r/battlebots provide a large and active community where you can find discussions on various aspects of robot combat, including motor selection and mount design. The Robot Combat Wiki serves as a comprehensive repository of information and also lists numerous online communities, including forums, Facebook groups, and Discord servers, categorized by weight class, region, and specific interests. Consider exploring the VEX Forum and the RobotShop Community Forum for additional discussions and technical insights. Local or regional combat robotics groups, often found through the Robot Combat Wiki, can also provide valuable in-person connections and advice.   

Websites and Build Logs: Numerous websites and build logs document the journeys and lessons learned by battlebot teams. The "Ask Aaron" section on the Run Amok website is a highly regarded resource for technical advice on combat robot design. BattleBots Update offers news, analysis, and sometimes build information from the professional scene. Many successful teams, such as Hypershock and HUGE, maintain blogs or websites detailing their build processes, challenges, and solutions. Platforms like Hackaday.io host a wide variety of robot projects, including battlebots, with detailed build logs and component lists. Studying these resources can provide inspiration and practical guidance for your own project.  
 
Books and Articles: While the combat robotics field is constantly evolving, the fundamental principles of engineering and design remain timeless. The official BattleBots rulebooks are essential reading to ensure your robot complies with all regulations.1 Websites like Instructables feature numerous tutorials and articles on combat robot design and construction, covering a wide range of topics from basic concepts to advanced techniques and Make 2 are excellent resources for learning fundamental concepts and advanced techniques in combat robotics

---
# Driving
Servo.h to feed signal to esc. Continuously send signals to the esc to for reversing, and stop when you get a positive signal from the ouput wire of the esc.
You may implement a way to stop that continuous reverse signal, by checking if the motor has stopped by other means.

Or exclude this alltogether and implement a system of non reversible turning, i.e. if throttle is more than 1500 then none of the motors should reverse even when turning, and vice versa.
Potential issue that the turning would be very slow.


---

# Questions

## Drive
- Replace RS775 with BLDC while keeping the same gearbox. Check curves for BLDC about speed and torque and power to see if its viable
- Voltage double pe rpm double.
- Brushed esc ki rating kaise dekhte jab voltage double ho jaata, like since rpm double ho rahi, current utna hi rahega kya?(all while Power double ho rahi) and kya esc ki Watt limitation hoti? ki bas current limitation hoti jisse power limitation aati (Power = V * I )?
- Nayi ESC ka budget hai? and nayi 24V battery(ies) ka? motor to sahi hai RS7775 waali, and RPM bhi agar 24V pe chala rahe, and current bhi typically utna jyaada hoga nahi as Stall current 30A hai, rated current kuch 13A hi hai.
- Cytron ki ESC's kaam karengi, phookengi to nahi, due to inductance and what not...?

## Weapon Motor

- Agar BLDC to ESC kaise choose kare - current rating se. BLDC ki windings ki current sehne ki limitation hoti, and ek Voltage ki.
- Weapon Drum ki MOI pata lag jaaye, to usse time to reach full speed, or even just ki wo equation kya hogi?
- Kya load mein BLDC even apne highest power tak pahuch paati

---

Ask about the different welding techniques that are available.

## Chassis
- Bevel gears (or stacked) for shock absorbing
- UHMW Washers for friction reduce (when turning there would be friction, on the opp side to the 'wall' that we are turning to)

---

For upsizing and downsizing, for only the most important parts, like shaft etc, use (scale)^(1.5); scale = (mass ratio)^1/3
Spin up should be 4 seconds

Weight optimization through cad softwares (Voids for inside panels, if there are, and other mounts)
Center of Mass dono wheels se same distance taaki same traction aaye dono wheels pe
Center of Mass slightly(u*h) forward than wheel center - isse bot tilt backwards nahi karega
To implement an invertible design by using wheels that are taller than the robot chassis
If the front side of robot has a tall chassis, but not its back side, then another option is to use 2 drive wheels in the back, and skids in the front.

30-30-25-15 rule:
	- 30 to drive system (motors, transmissions and wheels)
	- 30 to weapon system (weapon, motor, transmission0
	- 25 to structure and armour (always between 25 to 40)
	- 15 to battery and electronics
For Drumbot 20-35-30-15


Our current bot
- Drive System = 2.5kg (~30%)

Abhi humara bot lagbhag 9 kg ka hai, jabki humne Aluminium side panels bhi nahi daale hai, and even humara drum bhi utna heavy nahi hai, usme aur weight(ya MOI agar Drum weapon hi ditch kar rahe). RioBotz ke guide mein drumbot ke liye kuch aisa general rule hai ki 20% drive system, 35% weapon system, 30% armour and chassis, and baaki ka 15% electronics...
8KG ke liye humari drive and chassis bahut jyaada weight le rahi, weapon system ke liye weight bach hi nahi raha, jooki drum bot ke liye aur important hai(agli paragraph mein explain kiya hai), ek option hai ki chassis and drive pura redesign kare, 8kg ke liye; yaa phir same chassis and drive motors se 15kg mein jaaye...

hume drum ki MOI badhani hi padegi, whether mass se ya uske design se, kyunki hum weapon ko ekdum hi jyaada spin nahi kar sakte, usse 'bite' khatam ho jaayegi, like agar jyaada hi speed hui weapon ki, then drum would act almost more as a grinder, wo chew karega material, jabki hume chahiye ki ek bada hit mein energy disscipate kare dusre bot ko, which is what wins matches. High weapon speed ka yeh bhi hai ki usse air drag jyaada aata, bearings jaldi kharab hoti blah blah. Basically yeh ki hum weapon ki spin speed se agar uskme energy storage badhaye, to usse disadvantages bhi hai. (Read here: http://runamok.tech/AskAaron/spinner_FAQ.html)

