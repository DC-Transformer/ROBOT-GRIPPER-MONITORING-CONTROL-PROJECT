# PROJECT DESCRIPTION
The robotic arms play a crucial role in accurately handling and transferring components along the assembly line. Inconsistencies can occur when the grippers fail to pick up the correct object or does not pick up any object at all. These issues not only reduce productivity but can also lead to costly rework and wasted materials. The purpose of this project is to investigate and address the cause of gripper inaccuracies in robotic arms to ensure reliable handling. By developing an object detection solution, we will minimize errors that cause assembly line disruptions. Our solution will ultimately enhance the efficiency and reliability of the assembly process.

# SYSTEM ARCHITECTURE
The image below shows how each device will interact with each other:
<img width="1920" height="1080" alt="SYSTEM ARCHITECTURE DIAGRAM" src="https://github.com/user-attachments/assets/2a3befe1-aa17-40bf-b3f9-5fb9d447810c" />

- The arm will use 2 servos (1 to grab, 1 to lift)
- Each servo will have its current monitored
- The servo controlling the gripper will close until it detects a current spike, indicating that the part is secure
- The angle of the gripper servo will be saved
- The servo lifting the gripper will rotate, and the current needed to move the part will be monitored
- The gripper servo angle and the lifting servo current will be matched to the saved values for each part to determine if the correct part was carried

# REQUIREMENTS, SPECIFICATIONS, AND VERIFICATION
- System must react in real time
- Must withstand normal industrial conditions
- If current part is correct, then gripper will hold
- If current part is incorrect, an alarm will be triggered
- The system will only be trained to detect 2 parts for the sake of the project, but more can be added

# SELECTED HARDWARE, API, AND TOOLS
- ACS712 current sensor (2x)
- STM32 "blue pill" MCU (1x)
- Micro servo motor (2x)
- USB to TTL adapter (1x)
- STM32CUBEIDE
- FreeRTOS API

# REFERENCES
- Lectures and labs from Embedded Parallel Computing Course
- https://deepbluembedded.com/stm32-servo-motor-control-with-pwm-servo-library-examples-code/
- https://www.micropeta.com/video55
