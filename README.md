# 2-Digit-BCD-Up-Counter
A project done for the Digital Electronics module | Year 1 Semester 2 |

# 1. INTRODUCTION
BCD counters are fundamental in digital systems which represent human readable decimal digits from 0 to 9 using binary representation. Unlike standard binary counters, a 2-digit BCD counter treats each digit as a 4-bit nibble that resets after reaching 9 (10012). Traditional counters continuously count and require manual monitoring. This can cause human errors such as inaccurate stopping and inefficient operation. This project focuses on design and simulating a programmable version that allows a user to preset a target value, which the system must automatically detect to halt operations using Proteus.

# 2. PROBLEM DEFINITION AND OBJECTIVES
In many digital counting and monitoring systems, it is necessary to accurately track numerical values and automatically stop the process when a predefined target is reached. The proposed system implements a programmable 2-digit BCD up-counter count from 00 to 99 using sequential logic and synchronous counting techniques. It is displayed on the seven-segment display. Comparator logic is used to compare the current count with a user-defined target value which automatically stops at target, while the control system manages Start, Stop, Pause, Resume, and Reset operations. It improves accuracy and reduces manual monitoring.

# 3. SYSTEM DESIGN AND CIRCUIT EXPLANATION
<img width="686" height="485" alt="image" src="https://github.com/user-attachments/assets/bfc76b2f-4273-4ffe-bd59-b12d42b94b06" />

3.1 System Architecture\
The proposed system consists of three main stages: the input Stage (clock generator, push buttons, and target logic states), the processing stage (74LS192 BCD counters, 74LS85 comparators, logic gates and flip-flop) and the output stage (two 7-segment displays and LED).

# 3.2 Two-Digit BCD Counter Implementation
Counting section was implemented using Two cascaded 74LS192 counters. One counter handles one’s digits and the other counter handles tens digits. The Carry output of first counter was connected to the clock input of second counter to count 00 to 99. All counters are connected to a common Reset push button to reset the display to 00.

# 3.3 Target Value Comparator
Used two 74LS85 comparators to compare current count and target value. Eight LogicState inputs were used to set the target value manually in BCD format. Equality outputs from both comparators were connected to an AND gate so that the final output becomes HIGH only when both digits of the current counter value match the preset target value.

# 3.4 Clock Control and Automatic Stop Mechanism
When the comparator output detects A = B, it activates a Flip-Flop that disables the clock pulse to the counters. As a result the counting operation automatically stopped and the final count value remains fixed on the display. This same signal activates when
the target is reached by blinking LED.

# 3.5 Output Display and Status Indication
The BCD outputs are sent to Seven-Segment Displays (using internal or external decoders like the 74LS47) to provide real-time visual feedback. Additionally a status LED was connected to the final output to indicate successful target detection.

# 5. OBSERVATIONS AND POSSIBLE ENHANCEMENTS
The simulation results show that the system performs with high accuracy, stability and reliability. The simulation only started when the start push button was pressed even though the run icon was also activated. The counter consistently stopped exactly at the predefined target value, confirming the correct operation of the comparator logic. Additionally, the reset and resume push buttons also worked properly during simulation. For future improvements, the system can be enhanced to include a ‘millisecond’ countdown running in parallel with the existing countdown. This would improve timing precision and make the system more suitable for real-time applications. Additionally, the circuit can be expanded with more precise optional features such as a buzzer along with an LED to give both sound and light signals when the target value is reached.

# 6. CONCLUSION
This project has successfully implemented a programmable BCD counter using TTL logic ICs. By integrating the 74LS192 counters r with 74LS85 comparators, the system is able to perform automatic stop operation without any software program involved.
