# Smart-Vacuum-Cleaner
There will be 6 nodes, 4 main and 2 for future development, the 4 main nodes are :

1- UltraSonic node > collects distace data from sensor and publishes it to the control node through the sensor topic

2- IR node > collects data from senstor and publishes it to the feedback topic

3- Control node > subscribe from the UltraSonic node and makes all the prcessing needed "the main brain", and then publishes to the motor node through the command topic

4- Motor node > subscribe from the control node through the command topic and translate this message into a physical action

5- Navigation > for path planning , waypointing and mapping

6- logging > subscribe to all importangt topics for debugging -RViz-

There will be 3 main topics:

1- Sensor Topic : from Ultrasonic node to Control node, carries the distance message.

2- Command Topic : from Control node to Motor node, carries the linear and angular velocities.

3- Feedback Topic : from IR node to Control node, carries float (velocity)
