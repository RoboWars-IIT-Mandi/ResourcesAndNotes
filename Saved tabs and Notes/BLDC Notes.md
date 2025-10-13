- Lookup the theoretical equations of BLDC motors, mostly regarding the heat generated, we already have the efficiency and enerfy curve, maybe that would help? Check the JPL EELS paper, or the Rover playlist on BLDC
- For choosing motors of different kV... un motors ko calculator mein daalke dekho ki different gear ratios aur volatage mein changes karke kya effect hoga, and heat output dekhna ho then Resitance pata hogi motors ki to unse calculate kar lena ki relatively difference kya hoga.
- Hobby BLDC's are thermally constrained, i.e. Max power outut fix rehti, and the ratings jo rehte about continuous current are when used on a Helicopter with LiPo for the duration of flight only - i.e. weight of BLDC (and the shape - like added mechanical fans etc) ko dekhkar motor choose karo

- Check if true actually - Higer Kv have lower max Voltage, which is ideal as in our case we are doing 6S which is typically the lowest Max Voltage for BLDCs, thought is that we can churn the most power for the Voltage(i.e. 24 in our case). How does this affect the other characteristics of the motor, surely there should be implications? Check [Vedder article](https://vedder.se/2014/10/chosing-the-right-bldc-motor-and-battery-setup-for-an-electric-skateboard/) for choosing skateboard motors. Agar motor is rated for a higher Voltage than what we are running on, does this mean that the motor just got more inefficient? Since heat loss is I^2R, and it would be same irrespective of Voltage??(Think in terms of resistance, as Resistance squared hota for difference between motors of same dimension but different kv i.e. different max voltage)

- BLDC ki max speed (unloaded) tab hoti jab back emf is equal to supply voltage. Torque is prop to amount of current flowing. At no load max speed, no diff in voltage b/w voltage of motor and supply, hence no current, hence no torque.\
Torque is thermally contrained. This thermally constrained torque is rated torque. Max speed at which motor can operate forever at its rated torque is base speed.\
OR THe base speed (also called the rated or nominal speed) is the top speed at which a brushless motor can achieve at it's 'rated torque'. The 'rated torque' is the torque that a motor can output indefinitely without overheating.\
As a rule of thumb, the rated current, and therefore torque output, of a hobbyist motor will be around one third that of the peak torque value, or around two thirds with aggressive forced air cooling.\
The best way to keep your motor cool is to use a motor big enough to handle the load, run it at the highest voltage you can (usually 12s) and gear it appropriately so that your target top speed is ~80% of your esc's max erpm.

---

- https://www.nmotion.in/products/ncoder-5047
Rover team has contacts with this company, might get a discount - used in Vesc

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

---

## Saved Tabs
New Tab : chrome://newtab/
Editing BattleBot/Saved tabs and Notes/BattleBot BLDC.md at main · dhakkann/BattleBot : https://github.com/dhakkann/BattleBot/edit/main/Saved%20tabs%20and%20Notes/BattleBot%20BLDC.md
Combat robot motors and controllers - The Ask Aaron Archives : http://runamok.tech/AskAaron/motors.html
Combat Robot Spinning Weapon Design - Ask Aaron : http://runamok.tech/AskAaron/spinner_FAQ.html
Combat Robot: Estimating Rotary Weapon Spin-up Time : http://runamok.tech/AskAaron/estimating_spinup.html
Things in Motion: Understanding BLDC (PMSM) electric motors: Base speed, no load speed and torque vs speed : https://things-in-motion.blogspot.com/2019/05/understanding-bldc-pmsm-electric-motors.html
Chosing the right BLDC motor and battery setup for an electric skateboard | Benjamin's robotics : https://vedder.se/2014/10/chosing-the-right-bldc-motor-and-battery-setup-for-an-electric-skateboard/
Is higher kv better in motors? - RC Groups : https://www.rcgroups.com/forums/showthread.php?3078773-Is-higher-kv-better-in-motors
Brushless Motor Power and Efficiency Calculations - Tyto Robotics : https://www.tytorobotics.com/blogs/articles/brushless-motor-power-and-efficiency-analysis
Scorpion HK5-4030-1005kv - Scorpion Power System : https://www.scorpionsystem.com/catalog/helicopter/HK5_series/HK5_40/HK5_4030_1005/
RC Electric Motors | Brushed & Brushless Motors | HobbyKing : https://hobbyking.com/en_us/power-systems/electric-motors.html
SURPASS HOBBY C5065 14pole Outrunner Brushless Motor for Fixed Wing AircraftΦ6.0*23mm 4.0mm Connector (335 KV) - Robu.in | Indian Online Store | RC Hobby | Robotics : https://robu.in/product/surpass-hobby-c5065-14pole-outrunner-brushless-moror-for-fixed-wing-aircraft%cf%866-023mm-4-0mm-connector-335-kv/#tab-product_download_66939_tab
Explore Diverse range of Drone Motor at Low Price in India : https://robu.in/product-category/drone-parts/drone-motor/page/3/?orderby=price-desc&q=%2Fproduct-category%2Fdrone-parts%2Fdrone-motor%2F&utm_source=bing&utm_medium=cpc&utm_campaign=PMax-Drone%20Parts%20%26%20Accessories&utm_term=robu.in&utm_content=Drone%20Motors
You searched for 6s 22.2v - Robu.in | Indian Online Store | RC Hobby | Robotics : https://robu.in/?s=6s+22.2v&post_type=product&dgwt_wcas=1
Brushed and Brushless ESCs - Google Sheets : https://docs.google.com/spreadsheets/d/1iXG_-U036u3jl0MuzTEPDbzxgZP-VuRlwGiqfNZMB4Q/edit?gid=0#gid=0
BBOX PLUTO H700 MOTOR : https://www.technobotix.in/products/bbox-pluto-h700-530kv-bldc-motor/1781252000001751669
HobbyKing Red Brick 200A (2~6S) ESC V2 : https://hobbyking.com/en_us/hobbyking-red-brick-200a-2-6s-esc-v2.html?___store=en_us
HobbyKing YEP 180A HV (4~14S) Brushless Speed Controller (OPTO) : https://hobbyking.com/en_us/yep-180a-hv-4-14s-brushless-speed-controller-opto.html
Red Brick 200 amp esc - Any good ? - RC Groups : https://www.rcgroups.com/forums/showthread.php?2478135-Red-Brick-200-amp-esc-Any-good
200A Budget F5B controller - RC Groups : https://www.rcgroups.com/forums/showthread.php?1508380-200A-Budget-F5B-controller&highlight=HK%20200
Hobbyking SS Series 190-200A ESC 7S what u think? - General - Electric - MSUK RC Car Forum : https://www.msuk-forum.co.uk/forums/topic/151918-hobbyking-ss-series-190-200a-esc-7s-what-u-think/
cajt/list_of_robot_electronics: A curated list of awesome open source electronic resources for robotics : https://github.com/cajt/list_of_robot_electronics
ELECTRONICS : https://www.technobotix.in/categories/ELECTRONICS/1781252000000901029
XC ESC – 12s 120A 48V 12HP Brushless DC Motor Electric Speed Controller — Draft : https://robu.in/product/brushless-dc-motor-electric-speed-controller/
XC ESC - Drone Electronic Speed Controller supplier : https://www.xc-esc.com/
XeRun 系列 : https://www.hobbywing.com/products?id=23
XeRun AXE PLUS R3 : https://www.hobbywing.com/products/xerunaxeplusr3
XeRun XR8 Plus G2S : https://www.hobbywing.com/products/xerun-xr8-plus-g2s40
XR8 Plus G2S ESC (2-6S) - HOBBYWING North America : https://www.hobbywingdirect.com/collections/xerun-xr8-esc/products/xerun-xr8-plus-g2s?variant=40122237714547
EzRun MAX6 G2 : https://www.hobbywing.com/products/ezrunmax6g2
FLASH HOBBY H600 bldc motor : https://www.technobotix.in/products/bbox-pluto-h600-550kv-bldc-motor/1781252000001751636
EzRunMAX8 G2S : https://www.hobbywing.com/products/ezrunmax8g2s
QuicRun WP 8BL150 G2 : https://www.hobbywing.com/products/quicrun-wp-8bl150-g2291
1900W High Temperature Resistance Skateboard Bldc Motor Brushless For Scooter : https://www.micro-bldcmotor.com/sale-34747851-1900w-high-temperature-resistance-skateboard-bldc-motor-brushless-for-scooter.html
Custom KV Sensored / Sensorless IP67 Robot Outer Rotor Brushless Dc Motor 24V : https://www.micro-bldcmotor.com/sale-34561844-custom-kv-sensored-sensorless-ip67-robot-outer-rotor-brushless-dc-motor-24v.html
The New and Improved Brushless Electric Scooter Power System Guide : 19 Steps (with Pictures) - Instructables : https://www.instructables.com/The-New-and-Improved-Brushless-Electric-Scooter-Po/
Make Your Own Miniature Electric Hub Motor : 14 Steps (with Pictures) - Instructables : https://www.instructables.com/Make-Your-Own-Miniature-Electric-Hub-Motor/
Sensorless Motor Control: Which Algorithm is Right for your motor? - Solo Motor Controllers : https://www.solomotorcontrollers.com/blog/sensorless/
Scorpion HKIV-4035-560KV - Scorpion Power System : https://www.scorpionsystem.com/catalog/helicopter/motors_4/hkiv-40/HKIV_4035_560/
