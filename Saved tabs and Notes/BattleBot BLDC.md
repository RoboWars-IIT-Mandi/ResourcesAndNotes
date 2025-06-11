- Weapon Drum ki MOI pata lag jaaye, to usse time to reach full speed, or even just speed, wo equation kya hogi?
- How to choose motor when the same motor has different kv ratings? Higer Kv have lower max Voltage, which is ideal as in our case we are doing 6S which is typically the lowest Max Voltage for BLDCs, thought is that we can churn the most power for the Voltage(i.e. 24 in our case). How does this affect the other characteristics of the motor, surely there should be implications? Check [Vedder article](https://vedder.se/2014/10/chosing-the-right-bldc-motor-and-battery-setup-for-an-electric-skateboard/) for choosing skateboard motors.

BLDC ki max speed (unloaded) tab hoti jab back emf is equal to supply voltage. Torque is prop to amount of current flowing. At no load max speed, no diff in voltage b/w voltage of motor and supply, hence no current, hence no torque.\
Torque is thermally contrained. This thermally constrained torque is rated torque. Max speed at which motor can operate forever at its rated torque is base speed.\
OR THe base speed (also called the rated or nominal speed) is the top speed at which a brushless motor can achieve at it's 'rated torque'. The 'rated torque' is the torque that a motor can output indefinitely without overheating.\
As a rule of thumb, the rated current, and therefore torque output, of a hobbyist motor will be around one third that of the peak torque value, or around two thirds with aggressive forced air cooling.\
The best way to keep your motor cool is to use a motor big enough to handle the load, run it at the highest voltage you can (usually 12s) and gear it appropriately so that your target top speed is ~80% of your esc's max erpm.
---

## ESC
- Should we consider whether tuning of ESC is available or not?
- Are the normal drone esc okay be used for our case, checkup SimonK and how its tuned
- Tekin
- Maytech
- Flipsky 75100 or 75200 or 75300 or 75350 (Overkill)


