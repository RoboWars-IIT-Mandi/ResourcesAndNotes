## Design Docs
Check AskAaron for that accelaration, and speed calculator

---
- Drive algos test karna
- Compare BLDC with DC about weight, price, responsiveness, low-end torque etc (would making custom solutions like encoders and drivers be viable)
- FailSafe - ki agar signal na aaye, tab bhi bot thoda movement dikhaye, such ki wo immobile na ho - but isme agar actually bot ko rokna then kya karna ispar sochna padega, has safety concerns

- For current drive motors, try the cytron drivers - will fix that stopping while reversing direction
- Replace RS775 with BLDC while keeping the same gearbox. Check curves for BLDC about speed and torque and power to see if its viable. Jyaada current ki esc ki jaroorat nahi, just reversible esc honi chahiye.
- Voltage double pe rpm double? Basically check the curves for BLDC while varying voltage
- Cytron ki nayi ESC's kaam karengi? phookengi to nahi, due to inductance and what not...?
- For new motor controller, to check if motors moving in sync?(i.e. straight chal rahe?

### Driving Soln for current esc
Servo.h to feed signal to esc. Continuously send signals to the esc to for reversing, and stop when you get a positive signal from the ouput wire of the esc. Motor energy lose karne agar Diodes laga rahe then kya effect hoga?\
We may implement a way to stop that continuous reverse signal, by checking if the motor has stopped by other means.\
Or exclude this alltogether and implement a system of non reversible turning, i.e. if throttle is more than 1500 then none of the motors should reverse even when turning, and vice versa.
Potential issue that the turning may be slower the requirement.

### Drive Chassis
The rubber tyres are really strong - don't really need to protect those - can remove the protection for it - will save much weight. But will have to search about how to couple it with the drive motors - problem is ki motor shaft directly attach ho rahi - pura impact motor pe jaayega - will have to find some other way to couple - Copperhead does it by having an axle shaft extusion from the chassis, on which the motor rests with needle bearing - wheel held axially by bolts. Problem would be having that extrusion axle part attached to the chassis

---

## Differential Drive Saved Tabs
NodeMCU custom builds : https://nodemcu-build.com/
2 wheel smooth differential steering system - Google Search : https://www.google.com/search?sca_esv=0c1395bd2e2481ba&rlz=1C1VDKB_enIN1049IN1049&sxsrf=AHTn8zoNF7KBLFlKjQryFmD0BvQ3dqVO_w:1744176841236&q=2+wheel+smooth+differential+steering+system&udm=2&fbs=ABzOT_Cen_XDZtKf_vBGcVfGecI24gcwiADvKL7ToV_4ZQb8U_wgDs7rj_aj9b2OrTsMajXgTpny9qDhAvv5Z8352xBDswVU93fJB6K69Xci_yHKAzJO7tVoPliOU2ugFI7FQEGMBpcTFq9dVgT_6i7cN0lw5KpK3Y_c5oZt-hz9catOqshfsD-CCdwhrOEy9bv0qDh-ZthmtRwbs6THyqOIuIVuY89Ng5L3YNnGRTro5z-yXcxb0RM&sa=X&ved=2ahUKEwi0nbCIncqMAxUpcGwGHfJ0BDoQtKgLegQIEBAB&biw=392&bih=688&dpr=2.75
CN101332835A - Differential steering mechanism - Google Patents : https://patents.google.com/patent/CN101332835A/en
Experimental Comparison of Skid Steering Vs. Explicit Steering for a Wheeled Mobile Robot - Robotics Institute Carnegie Mellon University : https://www.ri.cmu.edu/publications/experimental-comparison-of-skid-steering-vs-explicit-steering-for-a-wheeled-mobile-robot/
How does your car take a turn smoothly - The Differential - Team-BHP : https://www.team-bhp.com/forum/technical-stuff/11958-how-does-your-car-take-turn-smoothly-differential.html
US3506079A - Six-wheeled vehicle with independent wheel suspension - Google Patents : https://patents.google.com/patent/US3506079
How Differential Steering Works | Goally TV : https://tv.getgoally.com/chill-zone/vintage%20cars/how-differential-steering-works
403 Forbidden : https://www.lynxmotion.com/c-30-a4wd1-rovers.aspx
RCArduino: RC Arduino Robot : https://rcarduino.blogspot.com/2012/05/rc-arduino-robot.html
A Systems Approach to Smooth Steering | OEM Off-Highway : https://www.oemoffhighway.com/home/article/10166537/a-systems-approach-to-smooth-steering
Why is differential steering with 2 passive (non caster wheel) not used? - Other Hardware / Robotics - Arduino Forum : https://forum.arduino.cc/t/why-is-differential-steering-with-2-passive-non-caster-wheel-not-used/919564/10
Two wheeled differential drive robot  | Download Scientific Diagram : https://www.researchgate.net/figure/Two-wheeled-differential-drive-robot_fig1_290304179
Study on Differential Assist Steering System with Double In‐Wheel Motors with Intelligent Controller - Li - 2015 - Mathematical Problems in Engineering - Wiley Online Library : https://onlinelibrary.wiley.com/doi/10.1155/2015/910230
Differential Steering vs. Skid Steering : r/robotics : https://www.reddit.com/r/robotics/comments/181uhqo/differential_steering_vs_skid_steering/?rdt=39442
ARDUINO - Google Drive : https://drive.google.com/drive/u/0/folders/1zhWFlHDuPBDP02ZoSGs2hpzbGMdcg89-
Computer controlled steering system for vehicles having two independently driven wheels - ScienceDirect : https://www.sciencedirect.com/science/article/abs/pii/S0168169903000814
System Modeling: Path Tracking for Differential Steering Drive Autonomous Robots - YouTube : https://www.youtube.com/watch?v=Lu1jH2q-MUE
Kinematics of Differential Drive Robots and Odometry - YouTube : https://www.youtube.com/watch?v=RZlZcDxQ8P4&t=1757s
icckinematics.pdf : https://www.cs.columbia.edu/~allen/F17/NOTES/icckinematics.pdf
ESP8266 NodeMCU PWM with Arduino IDE - Dim LED (Analog Output) | Random Nerd Tutorials : https://randomnerdtutorials.com/esp8266-pwm-arduino-ide/
ESP8266 GPIO Behaviour at Boot : https://rabbithole.wwwdotorg.org/2017/03/28/esp8266-gpio.html
ESP8266 Pinout Reference: Which GPIO pins should you use? | Random Nerd Tutorials : https://randomnerdtutorials.com/esp8266-pinout-reference-gpios/
Using Diamond Coordinates to Power a Differential Drive.doc : https://latiful.hayat.web.id/wp-content/uploads/2020/06/Using-Diamond-Coordinates-to-Power-a-Differential-Drive.pdf
Tracking Control for Differential-Drive Mobile Robots With Diamond-Shaped Input Constraints | Request PDF : https://www.researchgate.net/publication/264243182_Tracking_Control_for_Differential-Drive_Mobile_Robots_With_Diamond-Shaped_Input_Constraints
Lesson 102: Using ZK-5DA to control 2 DC Motor each 4A | Robojax.com : https://robojax.com/course1/?vid=lecture102#google_vignette
Skid steer controller · Issue #100 · ros-controls/ros_controllers : https://github.com/ros-controls/ros_controllers/issues/100
New Tab : chrome://newtab/


---

## Drive Tabs
BattleBot/Saved tabs and Notes/BattleBot Drive.md at main · dhakkann/BattleBot : https://github.com/dhakkann/BattleBot/blob/main/Saved%20tabs%20and%20Notes/BattleBot%20Drive.md
Brushless ESC Becomes Dual-Motor Brushed ESC With A Few Changes | Hackaday : https://hackaday.com/2024/02/15/brushless-esc-becomes-dual-motor-brushed-esc-with-a-few-changes/
frank26080115/Hydra-Dual-Brushed-Motor-ESC: Dual brushed motor ESC firmware compatible with brushless motor ESCs : https://github.com/frank26080115/Hydra-Dual-Brushed-Motor-ESC
Other Hardware Hacking · frank26080115/Hydra-Dual-Brushed-Motor-ESC Wiki : https://github.com/frank26080115/Hydra-Dual-Brushed-Motor-ESC/wiki/Other-Hardware-Hacking
Note: capacitor must be placed at power input · Issue #11 · frank26080115/Hydra-Dual-Brushed-Motor-ESC : https://github.com/frank26080115/Hydra-Dual-Brushed-Motor-ESC/issues/11
Other Hardware Hacking · frank26080115/Hydra-Dual-Brushed-Motor-ESC Wiki : https://github.com/frank26080115/Hydra-Dual-Brushed-Motor-ESC/wiki/Other-Hardware-Hacking
Sensorless Brushless Can’t Even | geeks have feelings : https://geekshavefeelings.com/posts/2016/sensorless-brushless-cant-even/
The Overhaul 2 Design & Build Series: #sadbot2016, The Untold Story; Or, How to Be a Brushless Hipster; Tuning the SimonK Firmware for Robot Drive – Equals Zero : https://www.etotheipiplusone.net/?p=3985
Issues · amcchord/MegaBrush : https://github.com/amcchord/MegaBrush/issues
Talon SRX: Advanced Smart Speed Motor Controller for Robotics | CTR El – CTR Electronics : https://store.ctr-electronics.com/products/talon-srx
Buy Heavy Duty Cytron Motor Drivers in INDIA at best price : https://robu.in/product-category/dc-motors/motor-drivers/cytron-motor-drivers/?orderby=price&q=%2Fproduct-category%2Fdc-motors%2Fmotor-drivers%2Fcytron-motor-drivers%2F
Buy Cytron 20Amp 6V-30V DC Motor Driver MD20A at Best Price : https://robu.in/product/cytron-20amp-6v-30v-dc-motor-driver-md20a/
Cytron 20Amp 6V-30V DC Motor Driver : https://robu.in/product/cytron-20amp-6v-30v-dc-motor-driver-2-channels/
TVS diode across motor leads failing short. How to protect MOSFET from motor back EMF? - Electrical Engineering Stack Exchange : https://electronics.stackexchange.com/questions/641201/tvs-diode-across-motor-leads-failing-short-how-to-protect-mosfet-from-motor-bac
Cytron Design: DC Motor Driver - How it works | RobotShop Community : https://community.robotshop.com/blog/show/brushed-dc-motor-driver-explained-part-1
EEVblog 1409 - The Dangers of Inductor Back EMF - YouTube : https://www.youtube.com/watch?v=hReCPMIcLHg&t=1013s
Back EMF protection diodes with inductive loads | PICAXE Forum : https://picaxeforum.co.uk/threads/back-emf-protection-diodes-with-inductive-loads.23155/
Tutorial - Experiment 7 - Bi-directional Control Of Motors And The H-Bridge : https://www.learn-c.com/experiment7.htm
Motor Driver keeps dying/frying driving a worm gear motor – tlfong01.blog : https://tlfong01.blog/2021/05/13/motor-driver-keeps-dying-frying-driving-a-worm-gear-motor-3/
Smart car BTN7971B dual motor drive D car balanced car group E motor d – Inkocean Technologies : https://inkocean.in/products/smart-car-btn7971b-dual-motor-drive-d-car-balanced-car-group-e-motor-drive-module-motor-drive?variant=20121044090998&country=IN&currency=INR&utm_medium=product_sync&utm_source=google&utm_content=sag_organic&utm_campaign=sag_organic
DRV88703.6-A Brushed DC Motor Driver (PWM Control) datasheet (Rev. B) : https://www.ti.com/lit/ds/symlink/drv8870.pdf?ts=1746864692490&ref_url=https%253A%252F%252Fsearch.brave.com%252F
H-Bridge protection from DC motor noise and regen - Page 1 : https://www.eevblog.com/forum/projects/h-bridge-dc-motor-surge-protection-active-clamp/
motor formulas / General Science and Electronics / Forums | 4hv.org : https://4hv.org/e107_plugins/forum/forum_viewtopic.php?p=1&id=87193#post-87209
