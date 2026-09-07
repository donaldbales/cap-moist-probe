## cap-moist-probe

# I<sup>2</sup>C Capacitive Moisture Probe

This is an electronics and software project to build an 8 inch capacitive moisture probe using off-the-shelf I2C sensors and parts from Adafruit paired with a Raspberry Pi 3 (RPi).

The soil sensor is functionally 2 inches long. I plan to stack four of them vertically around a fiberglass rod so they cover an 8 inch rise. The sensors have four possible addresses. In this design, I will use one 5 port passive hub to combine the four sensors. The hub will in turn be connected into an I<sup>2</sup>C active terminator to allow for a distance of more than one meter for the I<sup>2</sup>C line from the RPi. 

Since the soil sensors have 4 possible addresses, and an 8 port multiplexer is available, it is possible to stack 32 sensors for a probe that would be 64 inches long.

## Parts List
This is a partial list. Only the major components.

4 - Adafruit STEMMA Soil Sensor - I2C Capacitive Moisture Sensor - JST PH 2mm $8/ea.    https://www.adafruit.com/product/4026

1 - Adafruit Qwiic / Stemma QT 5 Port Hub $3/ea.   
https://www.adafruit.com/product/5625

1 - Adafruit LTC4311 I2C Extender / Active Terminator - STEMMA QT / Qwiic $10/ea.  
https://www.adafruit.com/product/4756

## Alternative Parts
You can use one of these multiplexors to stack more than 4 sensors.

Adafruit PCA9546 4-Channel STEMMA QT / Qwiic I2C Multiplexer - TCA9546A Compatible $4/ea.  
https://www.adafruit.com/product/5664

Adafruit PCA9548 8-Channel STEMMA QT / Qwiic I2C Multiplexer - TCA9548A Compatible $7/ea.  
https://www.adafruit.com/product/5626

## Experiments
In order to determine whether or not this probe will work, I need to perform the following experiments:

1. Does coating the electronics part of the sensor with a water protective coating, for example: FlexSeal, change the sensor's capacitive reactance?

2. Does fastening the sensor to a fiberglass rod change the sensor's capacitive reactance?

3. Is the probe: four sensors fastened to a fiberglass rod, coated with a water proof coating, connected to a five port passive hub, addressable and readable from a Raspberry Pi 3?

4. Does the probe work in a test environment where it is immersed in a tall container filled with varying levels of water?

5. Is the probe, connected to an I<sup>2</sup>C active terminator addressable over 100 feet of four pair cable from a RPi?

6. How well does the probe work when put into 8 inches of soil in the garden?

## Software
For each experiment, I will write a separate program in Python to collect the sensor(s') data from a Raspberry Pi 3. Why Python? Because Python is a very approachable programming language, originally designed as a language to teach programming and, Adafruit has open-source software available to address each of the sensors is sells.

