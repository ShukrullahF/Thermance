# Thermance
Thermance is a project where we created an automatic thermometer. The purpose of this project was to be able to measure body temperature without any human close contact.
Automatic IR thermometer
Ali Alagha, Shukrullah Fayazi, Jesper Dahlström, Alexander Lundström
 Abstract
Medical technology today is getting more and more complicated out of a user perspective and there are a lot of separate machines for different purposes. For hospital personnel especially, it is very difficult to keep track of and to learn how all the devices work. We want to merge and connect different equipment to the same device. Combining a carbon dioxide meter with a thermometer, which can detect the temperature of a person as well as the temperature of a room will facilitate the work for the staff.
Introduction
The society we live in today requires our technical products to be fast, efficient and user friendly. Also, in times of a global pandemic it is important to keep physical distance to other people, especially in public environments. One method to examine quickly whether a person is completely healthy or not is to measure their body temperature and watch for fever. This is a common method used in public places e.g. hospitals, airports and events. This method requires another person to hold a thermometer against the examined person's forehead, which breaks the rule of physical distancing. Alternative solutions to this type of easier examination for Covid-19 is to do a test with a manual thermometer. [1] A manual thermometer can show whether a person is having a fever or not, but requires close physical contact with another person.
Our solution to the problem where close interaction between people is forced because of the handheld thermometer is an automatic
Evaluation
We connect our device with a USB port to our PC. In this way, we power our circuit with 5V. Our program code is built in a way that when our PIR motion sensor registers a movement, it activates our thermal camera. When activated, our camera measures maximum, minimum, and average temperature of all the pixels in the image. The maximum temperature is what we use as a reference point for the person's body
thermometer, as physical distancing is recognised as an efficient method in limiting the spread of Covid-19. [2] Even when using a face mask, distancing is still recommended.[3] Therefore, a thermometer that works automatically without any human interaction is optimal in this case. This automatic thermometer will provide results of people's body temperatures, and also provide room temperature. A carbon dioxide sensor will be attached in an upcoming version, and will be used to tell whether a room needs ventilation. This measurement is important, as a high value may increase the risk of spreading diseases and viruses. [4]
Design
The device consists of an ESP32 microcontroller with built-in wifi and Bluetooth. Connected to the microcontroller is a thermal camera named Mlx90640 that contains a thermopile sensor. This camera measures the surface temperature of an object and forms a thermographic image with a resolution of 32x24 pixels. The component that starts the measurement is a PIR motion sensor, which is used to detect movement from humans and when detecting movement starts the measuring process. Fig(1) displays our circuit.
Fig (1)
temperature. Average temperature will be seen as the room temperature, and minimum temperature is the pixel containing the lowest temperature. When the temperature deviates and displays a value that is above our limit, it will start an alarm signal and a red light will appear.
One disadvantage with the performance of the thermal camera is that it requires the person to
 
stand very close to the camera to acquire an accurate result. The further away from the camera the person stands, the more inaccurate the result will be. On the other hand, the results are accurate when the person stands close to the camera as shown in fig(2) below.
Fig(2)
The usage of this device is ranging over a wide area. What makes the device so powerful is that it works automatically without the requirements of any user inputs other than their body in front of the camera. The image shown in fig(2) is
Sources and references
simply for surveillance. If a value input that is deviating abnormally occurs, the surveillor can examine the image and search for abnormalities.
The device will be further developed and include more features and components to display more measurements as well as include storage of input data. One key component that will be included further on is a carbon dioxide sensor.
Conclusion
The idea of putting two devices together that measure different values will enhance both the safety in a medical room as well as simplify the work for personnel. Primarily the thermometer will assure that a person has adequate body temperature. Secondly the thermometer together with the carbon dioxide meter will ensure that the temperature as well as air flow in a room is sufficient, and reduce further risk of spreading infections. The usage areas of this device are of a wide range.
 [1] https://www.folkhalsomyndigheten.se/the-public-health-agency-of-sweden/communicable-disease-control/ covid-19/covid-19-testing/screening-at-workplaces-and-schools/ [12/10 -21 10:45]
[2] https://www.who.int/westernpacific/emergencies/covid-19/information/physical-distancing [12/10 -21 10:00] [3] https://www.cdc.gov/coronavirus/2019-ncov/prevent-getting-sick/prevention.html#stay6ft%20
[12/10 -21 10:15]
[4] https://www.rotronic.com/en/humidity-measurement-feuchtemessung-temperaturmessungs/co2? fbclid=IwAR1OgWMEgaMm0JAEDzEWzmromXZ3eFqyL7C2uOT2uSuyemHsNw1VChf4604 [12/10 -21 14:00]
