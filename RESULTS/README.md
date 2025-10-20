# RESULTS
We were unable to get the original analog current sensor to work, so we switched to using a digital current sensor (INA219), and we had no issues with it. It worked for both baremetal and RTOS.

We also used the INA219 libary to read the current. We had a issue when we wanted to move the code from the while loop into a function that the RTOS task can call (float CURRENT_READ() ), where the initialization functions wouldn't work unless they were a part of the function, which meant the sensor was getting reinitialized every time.

Printing of current while servo motor is still and moving:
![WEEK 3 RESULTS](https://github.com/user-attachments/assets/d71d1feb-417a-47cd-aa80-252b6d2b2697)
