# RESULTS
The 2 tasks were created, and they both work, and the context switching is also displayed.

The sensing task (SENSOR_READ_TASK) reads the current of the servo, prints the result, and returns the result to a local variable, then the task moves it to a global variable.

The actuating task (ACTUATE) reads the global variable into a local variable, then checks if it's greater than 0.1, and runs the TRIGGER() function if true.

The TRIGGER() function only prints "ACTUATING NOW" for now, but it represents that something happens when a condition is met.

Basically it will print "ACTUATING NOW" when the servo is moving, since the current will be greater than 0.1A when moving.

For now the servo is controlled by a external servo tester for now, but the final version will be controlled directly with the STM32 Blue Pill MCU.

Tasks being run and switched every 500ms:

![Recording 2025-10-21 181604](https://github.com/user-attachments/assets/5afacd01-4ae4-4856-b81c-5786b4154e39)
