Dikkat kahi bhi hoti to heat ki hoti\

## Things to do
- Distibute Tasks between peeps
- New aluminium chassis design and fabrication
- Old Chassis to running condition, maybe even make it compatible with the new weapon motor. But it's a hassle to assemble it, really. Check if the chassis is bent, but before investigating on this, try to make better mounts for the drive motors.
- Fresher's ke liye readme
- Spinner design
- Spon dhundhna (check notes folder for potential spons)
- Events/Competitions ke baare mein research karna - approximate dates, specific rules (like BITS Hyd mein weight advantage), prize money and logistics, feasibility, and calendars match karna regarding Vacay and holidays and travel {work could be split between members}
- New members laane
- Freshers ko recruit karna
- Ask about the different welding techniques that are available. Ask about all the fabrication options available at campus.
- Ask where they get raw materials and other equipments for rover
- Drive algo kaunsa use karna chahiye, check which feels more natural - channel mixing from TX; Steering logic with simple clipping; Steering logic with scaled clipping; and finally that interpolation as mentioned in paper (complete implementation) - Check UKD Gemini chat
## Notes and links

- [BLDC Notes](Saved%20tabs%20and%20Notes/BLDC%20Notes.md)
- [Chassis Notes](Saved%20tabs%20and%20Notes/Chassis%20Notes.md)
- [Drive Notes](Saved%20tabs%20and%20Notes/Drive%20Notes.md)
- [Guides Notes](Saved%20tabs%20and%20Notes/Guides%20Notes.md)
- [Spinner Notes](Saved%20tabs%20and%20Notes/Spinner%20Notes.md)
- [Spon Notes](Saved%20tabs%20and%20Notes/Spon%20Notes.md)
- [Technical Fest Notes](Saved%20tabs%20and%20Notes/Technical%20Fest%20Notes.md)

## Resources
- Check the main folder for guides
- Check the saved tabs
- Review the YouTube playlist
- Saved Reddit comments/Posts
- Monash Rover YouTube tutorials - https://www.youtube.com/playlist?list=PL5qSL2ZI1kxaLx8j7aXUSWI0z1PuXzNJ6

---
## MISC

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

