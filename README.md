# 2-Digit-BCD-Up-Counter
1. INTRODUCTION\
BCD counters are fundamental in digital systems which represent human readable decimal digits from 0 to 9 using binary representation. Unlike standard binary counters, a 2-digit BCD counter treats each digit as a 4-bit nibble that resets after reaching 9 (10012). Traditional counters continuously count and require manual monitoring. This can cause human errors such as inaccurate stopping and inefficient operation. This project focuses on design and simulating a programmable version that allows a user to preset a target value, which the system must automatically detect to halt operations using Proteus.\

2. PROBLEM DEFINITION AND OBJECTIVES\
In many digital counting and monitoring systems, it is necessary to accurately track numerical values and automatically stop the process when a predefined target is reached. The proposed system implements a programmable 2-digit BCD up-counter count from 00 to 99 using sequential logic and synchronous counting techniques. It is displayed on the seven-segment display. Comparator logic is used to compare the current count with a user-defined target value which automatically stops at target, while the control system manages Start, Stop, Pause, Resume, and Reset operations. It improves accuracy and reduces manual monitoring.\

3. SYSTEM DESIGN AND CIRCUIT EXPLANATION
