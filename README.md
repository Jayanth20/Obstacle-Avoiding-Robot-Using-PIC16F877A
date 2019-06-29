# Obstacle-Avoiding-Robot-Using-PIC16F877A.
Obstacle Avoiding Robot is a mini project written in embedded C for ECE1005. 
This Project runs on PIC 16F877A.

**Hardware:**
1. PIC16F877A
2. IR Sensor (2Nos)
3. Ultrasonic Sensor (1Nos)
4. DC Gear Motor (2Nos)
5. L293D Motor Driver
6. Chaises (You can also build your own using cardboards)
7. Power bank (Any available power source)

**Circuit Diagram:**
[circuit](pics/circuit.jpg)

**Concept of Obstacle Avoiding Robot:**

The concept of Obstacle Avoiding Robot is very simple. We use sensors to detect the presence of objects around the robot and use this data to not collide the robot over those objects. To detect an Object we can use any use sensors like IR sensor and Ultrasonic sensor.

In our robot we have used the US sensor as the front sensor and two IR sensor for the left and right respectively. The robot will move forward when there is no object present before it. So robot will move forward until the Ultrasonic (US) sensor detects any object.
[move forward until](pics/move-forward.png)

When an object is detected by the US sensor, it is time to change the direction of the robot. We can either turn left or right, to decide the turning direction we use the help of IR sensor to check if there is any object present near the Left or right side of the robot.
If there is an objected detected on the front and right side of the Robot, then the robot will come back and turn left. We make the robot to run backward for a certain distance so that it does not collide on the object while making the turn.
[go back and turn left](pics/move-left.png)

If there is an objected detected on the front and left side of the Robot, then the robot will come back and turn right.
[turn right](pics/move-right.png)

If the robot reaches a corner of the room it will sense object present in all four. In this case we have to drive the robot backward until any of the side becomes free.
[backward](pics/move-backward.png)

Another possible case is that there will be an object in front but there might not be any object neither in the left side nor on the right side, in this case we have to randomly turn in any of the direction. 
[left or right](pics/move-left-or-right.png)
