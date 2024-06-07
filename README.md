# PoC Automatic cam boarding count (Edge computing)
PoC´s of IA camera to count people and vehicles
This proof of concept aims to demonstrate the image analysis capabilities of the processors included in the current video surveillance cameras.

We have used an easy-to-use camera that includes several image analysis algorithms with object training and machine learning capabilities.

The prototype shown in the following video is an isolated system without an Internet connection. It is made to count the number of people and vehicles on board. 

This has been achieved with the following components:
* [Micro:bit](https://microbit.org/) A microcontroller send through an I2C type serial connection the command to set the mode of object recognition to the camera.
* [Huskylens camera of Gravity](https://www.dfrobot.com/product-1922.html). 
 * The image is analyzed locally, identifying people and vehicles. When one of these elements is identified. It will appear on the camera display in a frame with the object type text.
 * If the camera was previously trained to recognize one of these objects individually. It will appear a frame in blue and identified with a numbered label.
 * The camera transmits the meta-information of people and vehicles detected in real time to the microcontroller. The firmware retrieves the total detected objects and displays the number on a single digit display.

Schematic breadboard:



















To resolve this simple use case: count persons and vehicles on board. The firmware required is very simple:

