# Smart-Vacuum-Cleaner
There will be 5 nodes, 4 main and 2 for future development, the 4 main nodes are :

1- UltraSonic node > collects distace data from sensor and publishes it to the control node through the sensor topic

2- IR node > collects data from senstor and publishes it to the feedback topic

3- Motor node > subscribe from the UltraSonic node through the Sensor topic and translate this message into a physical action

4- Navigation > for path planning , waypointing and mapping

5- logging > subscribe to all importangt topics for debugging -RViz-

There will be 2 main topics:

1- Sensor Topic : from Ultrasonic node to Motor node, carries the distance message.

2- Feedback Topic : from IR node to Control node, carries float (velocity)
