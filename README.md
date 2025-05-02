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

- Voltage double pe rpm double?
- Brushed esc ki rating kaise dekhte jab voltage double ho jaata, like since rpm double ho rahi, current utna hi rahega kya?(all while Power double ho rahi) and kya esc ki Watt limitation hoti? ki bas current limitation hoti jisse power limitation aati (Power = V * I )?
- Nayi ESC ka budget hai? and nayi 24V battery(ies) ka? motor to sahi hai RS7775 waali, and RPM bhi agar 24V pe chala rahe, and current bhi typically utna jyaada hoga nahi as Stall current 30A hai, rated current kuch 13A hi hai.




