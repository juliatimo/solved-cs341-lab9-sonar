Download Link: https://assignmentchef.com/product/solved-cs341-lab9-sonar
<br>
In this lab, you will learn how to use a distance sensor to determine the speed and direction of a moving object. The starter code can be found on GitHub under Lab 9.

Background Information

The concept of sonar is pretty simple. We will output a wave for a brief period of time, the wave will bounce off of something, and return to us. If we keep track of how long we waited for, and we know the speed of a sound wave (343 m/s), we can calculate the distance the wave traveled using the general equation

Like this

where  is the distance to the object. Notice, we divide by two because we have the time the entire trip (to the object and back) took, not the time just to the object.

To find the time in Arduino, we will make use of the <a href="https://www.arduino.cc/reference/en/language/functions/advanced-io/pulsein/?setlang=it">pulseIn</a>() function. We connect a digital pin up to a distance sensor and call pulseIn, it watches how long the distance sensor is high for and returns that time in microseconds.

Setting Up the Sensor

The sensor’s circuit is quite simple. It just needs 5V, ground, and a wire to send its signal on.

Note: in tinkercad there are two distance sensors, make sure you use the one with only 3 pins.

The Code

In the starter code, the function ping(int pingPin) is already written for you. It will send out a signal on the sensor and calculate the distance from the sensor to the object the signal bounced off of.

In loop(), estimate the velocity of the object the sensor is detecting. A velocity of 0 means the object is the same distance away, a positive velocity means the  object is moving away, and a negative velocity means the object is coming closer. Print out the distance and velocity but keep your printout minimal as printing takes time. Something like this is fine:

D: 100 | V: -38.33

D: 278 | V: 59.33

D: 278 | V: 0.00

D: 286 | V: 2.67