# PROJECT DESCRIPTION
The robotic arms play a crucial role in accurately handling and transferring components along the assembly line. Inconsistencies can occur when the grippers fail to pick up the correct object or does not pick up any object at all. These issues not only reduce productivity but can also lead to costly rework and wasted materials. The purpose of this project is to investigate and address the cause of gripper inaccuracies in robotic arms to ensure reliable handling. By developing an object detection solution, we will minimize errors that cause assembly line disruptions. Our solution will ultimately enhance the efficiency and reliability of the assembly process.

# SYSTEM ARCHITECTURE
The image below shows how each device will interact with each other:
<img width="1920" height="1080" alt="SYSTEM ARCHITECTURE DIAGRAM" src="https://github.com/user-attachments/assets/2a3befe1-aa17-40bf-b3f9-5fb9d447810c" />

There will be 2 current sensors connected in series with the servos, which will connect to the MCU, which will determine the current at any time.

# REQUIREMENTS, SPECIFICATIONS, AND VERIFICATION
- System must react in real time
- If current part is correct, then gripper will hold
- If current part is incorrect, then gripper will release

# SELECTED HARDWARE, API, AND TOOLS
- ACS712 current sensor (2x)
- STM32 "blue pill" MCU (1x)
- Micro servo motor (2x)

# REFERENCES

- https://deepbluembedded.com/stm32-servo-motor-control-with-pwm-servo-library-examples-code/
- https://blog.embeddedexpert.io/?p=1687
