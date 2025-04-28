![][image1]

**SNTC**  
IIT Mandi

# Robo Wars

## **Project Proposal**

# **OVERVIEW**

This project aims to design, build, and operate a 8 kg combat robot known as a Drumbot, focusing on its application in competitive events. The Drumbot will feature a high-speed rotating drum as its primary weapon, capable of delivering powerful impacts to opponents.The goal is to create a strong, compact robot by selecting and assembling parts like motors, control systems, and protective armor. Through testing and improvements, the robot's performance will be fine-tuned for competition. This hands-on project will enhance understanding of robotics, control systems, and mechanical engineering, culminating in a demonstration of Drumbot's  competitive capabilities. Our bot is inspired by  ‘[minotaur](https://battlebots.fandom.com/wiki/Minotaur)’ battlebot .  
Our aim is to make a competition ready battlebot , which would represent our institute in various competitions all over the nation .  
Last but not least this project will start a legacy of battlebot in our institute which will benefit and help students learn and innovate year after year.

# **DESIGN** 

We chose a two-wheel drive system to maintain stability during weapon impacts. If the impulse  J  is vertical in the upward direction, as long as the spinning drum has solid ground supports that will transmit the entire impulse  J  without allowing the robot to tilt forward after the attack.

The drum weapon design features a wedge shape to improve energy transfer during impacts. This shape helps maximize tooth bite and keeps the drum balanced without extra counterweights. We will use Genetic Algorithms to optimize the design for better performance.

# **COMPONENTS SPECIFICATIONS**

* ## Transmitter and Receiver

A [transmitter](https://robu.in/product/flysky-fs-i6x-2-4ghz-10ch-afhds-2a-rc-transmitter-with-fs-ia10b-2-4ghz-10ch-receiver/) is a device that allows the user to send input signals to a receiver, which then controls various components based on the input. In a battlebot, the transmitter enables the user to control key functions such as movement and weapon activation.The receiver processes the signals and forwards them to the microcontroller, which then sends appropriate commands to the Electronic Speed Controllers (ESCs) and motors.

In our current battlebot, we use a single channel to control both drive motors for movement (forward, backward, left, and right), and a separate channel is used to control the weapon motor. However, we are using the Flysky FS-i6X 6-channel transmitter and receiver to allow for future upgrades, such as additional weapon systems, armor mechanisms, or other advanced features. This setup provides flexibility for future enhancements while keeping the current control system simple and effective.

* ## Microcontroller

The microcontroller acts as the brain of the battlebot, processing signals from the receiver to control the motors. It interprets commands from the  transmitter for both drive and weapon functions. For the drive motors, it adjusts speed and direction through the ESCs. For the weapon, it ensures the motor spins quickly for powerful strikes. The microcontroller also communicates with the gyroscope to maintain stability and improve balance during fast movements.

We are using the Teensy 4.0 Development Board because of its powerful processing capability, compact size, and ability to handle real-time tasks efficiently. It can easily manage high-speed communication with sensors.

* ## Electric Speed Controller

[Electronic Speed Controller](https://robu.in/product/hobbywing-quicrun-1625-25a-waterproof-brushed-electronic-speed-%E2%80%8B%E2%80%8Bcontroller/?) (ESC) controls the brushed DC motor based on signals from a microcontroller. The user’s commands are sent via a transmitter and received by a receiver module, which forwards them to the microcontroller. The microcontroller processes the input and generates a PWM signal that is sent to the ESC. The ESC interprets this signal to adjust the motor's speed and direction. 

As an ESC we are using a Hobbywing Quicrun 1625 60A , providing precise control for smooth operation of the battlebots.

* ## Motors 

[Drive Motor](https://roboticsdna.in/product/42gx-775-12v-1000-rpm-45mm-dia-planetary-gear-motor/?src=google&kwd=&adgroup=): This motor is responsible for the robot's movement, controlling the wheels or treads that allow it to navigate around the arena. The power and speed of the drive motors affect the robot’s agility, traction, and pushing power. Drive motors need to have the right balance of torque and speed to help the robot move smoothly and react quickly during a match. 

Weapon Motor: The weapon motor powers the spinning drum. It is designed for high-speed rotation to deliver powerful hits. The motor needs to provide enough power to spin the drum quickly and keep up the energy for repeated impacts during combat.

Since we are aiming for high torque and appropriate RPM for our bot, we are using a combination of Orange Planetary Gear DC Motor (12V, 370 RPM, 147.2 N-cm, PGM45775-19.2K) for the drive system. This motor provides the necessary torque for smooth movement and pushing power. For the weapon system, we are utilizing the 42GX-775 Planetary Gear Motor (12V, 1000 RPM, 45mm diameter), as it delivers the high RPM needed to ensure rapid weapon spin and impactful damage.

* ## Gyroscope

A gyroscope helps maintain balance and stability by tracking the robot's orientation. It provides real-time feedback to correct movements and keep the bot upright after impacts. The gyro also ensures smoother turns and better control, minimizing drifting during combat. Overall, it improves precision and agility.

We are using the MPU9250 gyro for its 9-axis sensing capabilities, combining a gyroscope, accelerometer, and magnetometer. It provides accurate orientation and stabilization data, helping our battlebot maintain balance and smooth movement during combat.  
Alternative for this gyro as it is out of stock is [HW290](https://robu.in/product/mpu6050hmc5883lbmp180-10dof-3-axis-gyro-3-axis-acceleration-3-axis-magnetic-field-air-pres/).

* ## Battery

We are using two 12v lipo [batteries](https://robu.in/product/orange-3300mah-3s-35c-80c-lithium-polymer-battery-pack-lipo/) , each to power drive and weapon system respectively.

# **MATERIALS** 

Tyres: Polyurethane, chosen for durability and traction. We have chosen nylon casted cylinders as alternative.

Body: Mild steel (½”\*½”, 2mm thick) for the frame, and aluminium sheets(2mm) for lightweight yet strong protection.

Skid Plates: Aluminium, providing a balance of strength and weight.

Drum and Shaft: Aluminium, selected for its light weight and sufficient strength, ideal for high-speed weapon performance.

# **Budget Breakdown**


| Components and Purchasing  links | Price | Quantity | Total |
| :---- | :---- | :---- | :---- |
| [Microcontroller](https://robu.in/product/teensy-4-0-development-board/?gad_source=1&gclid=CjwKCAjwuMC2BhA7EiwAmJKRrNMs2Dqu3TcorJ8jgyKNO6eeljNZAtf53hT1jHxSL6rpeat6A3YH5hoCfmcQAvD_BwE) | ₹2199 | 1 | ₹2199 |
|  [Weapon Motor](https://roboticsdna.in/product/42gx-775-12v-1000-rpm-45mm-dia-planetary-gear-motor/?src=google&kwd=&adgroup=) | ₹2500 | 1 | ₹2500 |
| [Gyroscope](https://www.electronicscomp.com/mpu9250-9-axis-attitude-gyro-accelerator-magnetometer-sensor-module?gad_source=1&gclid=Cj0KCQjwpP63BhDYARIsAOQkATY0tiv4pMRk_9rGWKbEu8hYiFa-3WMIANOPf817Q6joqogdtJBMZYwaAs5eEALw_wcB) | ₹446 | 1 | ₹446 |
| [PDB](https://robu.in/product/pdb-xt60-w-bec-5v-12v/?gad_source=1&gclid=CjwKCAjwuMC2BhA7EiwAmJKRrG1SGswle86TqswdKShPpvOt0WhObpqZpOB968JZA_v-cTevIgBbtBoCEcoQAvD_BwE) | ₹345 | 1 | ₹345 |
| [Battery](https://robu.in/product/orange-3300mah-3s-35c-80c-lithium-polymer-battery-pack-lipo/) | ₹2268 | 1 | ₹2268 |
| [Drive Motor](https://robu.in/product/orange-planetary-gear-dc-motor-12v-370-rpm-147-2-n-cm-pgm45775-19-2k/) | ₹2295 | 2 | ₹4590 |
| [ESC](https://robu.in/product/hobbywing-quicrun-1625-25a-waterproof-brushed-electronic-speed-%E2%80%8B%E2%80%8Bcontroller/?gad_source) | ₹2064 | 2 | ₹4128 |
|  |  |  |  |
| **Materials** | **Price/Kg** | **Weight** | **Total** |
| Aluminium (Drum+Body) | ₹540 | 3.5Kg | ₹1890 |
| Mild Steel (Frame) | ₹98 | 2Kg | ₹196 |
| Tyres (Polyurethane) | \- | \- | ₹730 |
| Miscellaneous (tyre grip, drum blades) | \- | \- | ₹700 |
| TOTAL(Components+Materials) |  |  | ₹19992 |

# **COMPETITIONS**

* IIT Delhi    **Tryst**    Robowars  29-31 MARCH(2024)  
* IIT Bombay   **Techfest**   Robowars   17-19 December(2024)  
* IIT BHU    **Technex'24**    Robowars  10 Feb-1 march,15-17 march (2024)  
  There are weight categories for battlebots , hence we have aimed for 8kg category.  
  


**Battlebot Simulator Video**

* [https://drive.google.com/file/d/1aYNq6\_ubTKao1L5ZGcgUKZAAo2ItcmoB/view?usp=drivesdk](https://drive.google.com/file/d/1c4CbtO1Sa86zPN8gB642vz4YVEWCa4pj/view?usp=drivesdk)  
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
  




# 

# 

# 

# 

# 

# 

# 

# 

# 

# 

TEAM INFORMATION

| Name | Roll Number |
| :---- | :---- |
| Rahul Patidar | B23284 |
| Gunjeet Kumawat | B23371 |
| V Shrenik | B23476 |
| Abhinav Choudhary | B23335 |
| Amar  | B23313 |
| Vishal  | B23440 |
| Sachit | B23291 |
| Alok Yadav  | B23426 |
| Prashasti Singh | B23224 |
| Jaya Pandey | B23444 |
| Nimit Garg | B23379 |
| Aditya | B23189 |
| Ketan Chandra | B23446 |
| Adit Raj | B23480 |

TIMELINE:  
[Click](https://picturesque-wishbone-802.notion.site/fd015ac590144ab390389788170d08df?v=79c67676d68b4032b10ade697e943d6d&pvs=4) for live timeline of the project

# **REFERENCES**

* [https://battlebots.fandom.com/wiki/Minotaur](https://battlebots.fandom.com/wiki/Minotaur)  
* [https://www.instructables.com/How-to-design-and-build-a-combat-robot/](https://www.instructables.com/How-to-design-and-build-a-combat-robot/)  
* [https://robotwars.fandom.com/wiki/Drums](https://robotwars.fandom.com/wiki/Drums)  
* [http://meggi.usuarios.rdc.puc-rio.br/paper/C146\_RG12\_Drum\_shape\_design\_and\_optimization.pdf](http://meggi.usuarios.rdc.puc-rio.br/paper/C146_RG12_Drum_shape_design_and_optimization.pdf)




[image1]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAnAAAAAHCAYAAACIq3DzAAAAQUlEQVR4Xu3WMQ0AIADAMFziCFGYgx8FLOnRZwo25l4HAICO8QYAAP5m4AAAYgwcAECMgQMAiDFwAAAxBg4AIOYClIUh9UOLBN8AAAAASUVORK5CYII=>