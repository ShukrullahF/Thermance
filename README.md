# Thermance
Thermance is a project where we created an automatic thermometer. The purpose of this project was to be able to measure body temperature without any human close contact.

Automatic IR thermometer 

Ali Alagha, Shukrullah Fayazi, Jesper Dahlström, Alexander Lundström



Abstract

There is a problem determining the temperature of a person whether it is in a hospital, an airport or another establishment. The problem is that it needs a staff person or an invasive method. The temperature measurement will be able to measure the temperature without a person measuring it or by an invasive method. By connecting a motion sensor with a temperature measurement device, we created a device that neither needed a person doing the measurement or an invasive method.     


Introduction

There is a pandemic in the world right now and people still feel the need to travel the world. There are a few characteristic symptoms related to the pandemic. Fever is one of the symptoms of the pandemic right now. You can’t travel if you are feverish. Making sure that a person doesn’t have a fever and is able to travel is our main purpose in our creation of the temperature measurement. We want to make the staff members feel as safe as they can by not catching the virus. Also, we want the passengers to feel safe and not harm them by an invasive method. The temperature measurement detect

There are a different number of alternative solutions to this problem at the moment. One of the other solutions is by using a handheld temperature device that looks like a gun. The reading of the temperature can be used with either thermal or IR thermometer. In this case you need a person to take the temperature and read the result [1][2]. The temperature can also be taken invasively, this is not very common at the airport. This is more common at the hospital or other health care institutions in comparison to the airport's temperature measurements [3]. 

Our solution to the stated problem is by combining a motion sensor and a thermal temperature device.  In our case we do not need a staff member controlling the temperature and they can be at a safe distance by not taking the temperature themselves. We have applied a diode system, where different colors represent different results depending on the color shown. Green for approved and red for denied entrance. If the passenger's temperature is approved by the system and the diodes connected to it, it is safe for the passenger to enter the airplane. Otherwise the diode will turn red and the temperature is not approved to enter the plane. 

Design

The device consists of an ESP32 microcontroller with built-in wifi and Bluetooth. Connected to the microcontroller is a thermal camera named Mlx90640 that contains a thermopile sensor. This camera measures the surface temperature of an object and forms a thermographic image with a resolution of 32x24 pixels. The component that starts the measurement is a PIR motion sensor, which is used to detect movement from humans and when detecting movement it starts the measuring process. We created a website that includes a surveillance and registration system. Fig (1) displays the finished product with the 3D printed box that carries all the components and makes it able to mount the device on the wall.
Fig (1)

Evaluation 

The device is connected via USB to a PC. In this way, we power the circuit with 5V. Our program code is built in a way that when our PIR motion sensor registers a movement, it activates our thermal camera. When activated, our camera measures maximum, minimum, and average temperature of all the pixels in the image. The maximum temperature is what we use as a reference point for the person's body temperature, whereas the minimum temperature is the pixel containing the lowest temperature. When the temperature deviates and displays a value that is above our limit, it will trigger the redlight. Otherwise the green light will appear. 

One disadvantage with the performance of the thermal camera is that it requires the person to stand very close to the camera to acquire an accurate result. The further away from the camera the person stands, the more inaccurate the result will be. On the other hand, the results are accurate when the person stands close to the camera as shown in fig(2) below.

The usage of this device is ranging over a wide area. What makes the device so powerful is that it works automatically without the requirements of any user inputs other than their body in front of the camera. The image shown in fig(3) is simply for surveillance. If a value input that is deviating abnormally occurs, the surveillor can examine the image and search for any abnormalities. 
Before making a measurement it is possible for the user to register their name and ID number, in this way it is possible to store results and connect those to unique users.

Conclusion

Combining a motion sensor and thermal temperature measurement device to facilitate the work with high body temperatures, mainly at airports.  The aim for this thermometer is for the temperature measurement to be handled with care and ensure that everyone can feel safer. To light up a diode will give the traveler an answer right away if it is possible for them to travel. By motion sensing and standing in front of the thermometer the diodes will brighten up. The color green indicates that your surface body temperature is approved whereas red indicates that your surface body temperature is too high to travel.

FOR FIGURES SEE SEPARATE DOCUMENT! 

Sources and references 

[1] https://www.cbc.ca/news/politics/airline-passenger-temperature-checks-1.5609564  (4/1-22, 10:42)
[2]https://www.flir.com/discover/instruments/whats-the-difference-between-ir-thermometers-and-thermal-cameras/ (4/1-22, 11:52)
[3] https://www.processindustryforum.com/article/invasive-temperature-measurement-vs-non-invasive-temperature-measurement-techniques (4/1-22, 10:55)
