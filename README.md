# Autonomous Vacuum Cleaner Project

This project demonstrates the use of ROS to build and control an autonomous vacuum cleaner capable of avoiding obstacles dynamically. Below is an overview of the ROS nodes and their functionality:

## Features

1. ** Obstacle Detection using Ultrasonic Sensor **

Node: ultrasonic_sensor_node

Functionality:

Continuously reads the distance between the sensor and the nearest obstacle or wall.

Publishes the readings to a dedicated ROS topic (/ultrasonic_distance).


Purpose:

Enables the control system to monitor the environment in real-time.




2. Control Node for Decision Making

Node: control_node

Functionality:

Subscribes to the ultrasonic sensor topic (/ultrasonic_distance) to receive distance readings.

Monitors the distance values and determines if the robot is approaching an obstacle.

Sends a signal to the motor driver via a topic (/motor_control) to:

Slow down when an obstacle is detected.

Stop if the obstacle is too close.



Purpose:

Manages the robot's movement based on real-time data from the sensors.




3. Motor Driver Communication

Node: motor_driver_node

Functionality:

Subscribes to the control topic (/motor_control) to receive speed and direction commands.

Adjusts the motor's speed and direction accordingly.


Purpose:

Executes movement commands, ensuring smooth operation of the vacuum cleaner.





Workflow

1. The ultrasonic sensor continuously publishes distance readings.


2. The control node monitors these readings and evaluates the proximity of obstacles.


3. Based on the obstacle's distance:

Commands to slow down or stop are sent to the motor driver.



4. The motor driver node adjusts the robot's movement accordingly.



Topics Used

Future Enhancements

Implementing mapping and localization for improved navigation.

Adding additional sensors for enhanced obstacle detection.
