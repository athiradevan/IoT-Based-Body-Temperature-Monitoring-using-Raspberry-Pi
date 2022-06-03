# IoT Based Contactless Body Temperature Monitoring 
<h3 align="left">About</h3>

IoT Based Contactless Body Temperature Monitoring using Raspberry Pi with Camera and Email Alert

* Body temperature is commonly evaluated with temperature devices and in this, the gadgets are equipped with non-contact infrared temperature sensors that can detect body temperature without requiring physical contact. If the temperature of any individual person exceeds the predetermined value, we will interface an IR temperature sensor and send email notifications with the image of the person. 
* The Internet of Things is altering our lives in today's world by producing a variety of technologies that can be monitored and controlled remotely. In this project, the Raspberry Pi, MLX90614, and PiCamera are used to create a temperature monitoring gadget with email alerts.


<h3 align="left">Components Required: </h3>

* Raspberry Pi 3 
* Pi Camera
* MLX90614 - IR temperature sensor
* Connecting wires
* Breadboard
* LED
* Connecting pins
* 220Ω or 1KΩresistor
* Power Supply (5V,2A/3A)

<h3 align="left"> Software Language used: Python</h3>

<h3 align="left">Sample code: </h3>

from smbus2 import SMBus

from mlx90614 import MLX90614

bus = SMBus(1)

sensor = MLX90614(bus, address=0x5A)

print "Ambient Temperature :", sensor.get_ambient()

print "Object Temperature :", sensor.get_object_1()

bus.close()

<h4 align="left">We make a new file name mlxread.py and write a sample program like above to check the data from the sensor. Once the file is created, we will run it with python extension python mlxread.py.</h4>

* Simply run the python code on the Pi once the hardware and software are ready. The temperature reading from the sensor will be printed.

* If the object temperature rises beyond the threshold, our Python application will take a picture with the camera, save it on the Raspberry Pi, and send it via email.




