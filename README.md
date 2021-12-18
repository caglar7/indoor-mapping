# indoor-mapping with arduino car

## **ABSTRACT**
In this project, we made an IoT system that does indoor mapping of a closed environment (mostly rooms) and measurements of elements such as air-quality, humidity and temperature. 
We used machine learning to make predictions of numbers of people can inhabit in these environments. For sketching maps, we used turtle module in python and to handle measured 
data, we used Firebase servers. A Nodemcu board is used to connect to Wi-Fi. Following images are for the nodemcu board and the arduino car.

<img src="images/nodemcu.png" height="250"> <img src="images/car_image1.png" height="250"> <img src="images/car_image2.png" height="250">

## **PROBLEM DEFINITION**
Collecting data from an environment remotely can be quite important in some applications. The air might be poisonous or the temperature might be at a risky level and we would also want to know how much space there is in an unknown environment. So, this project is for exploring purposes and make predictions on how many people can live in a certain area.
Measurements are recorded to the server and can be easily retrieved from the server to a computer that has the python code running. With this code, we are able to sketch the obtained distance measurements according to the car position and we can also monitor other types of measurements on the screen.

## **OPERATION**
Initially the arduino is programmed to make the car find the center point in any room it's stationed using its sensors. When the car is positioned on the center, it starts to take distance measurements while rotating from 0 to 359 degrees and it takes one measurement for each degree. Then it transfers these “angle” and “distance” values along with other measurements to the Firebase Database. For this database, the images below can be observed.

<img src="images/firebase1.png" height="250"> <img src="images/firebase2.png" height="250"> 

After all the measurements are obtained, program start drawing the map. This is done using Turtle Graphics module in python. These drawings are not 100% accurate since there will be some portion of wrong measurement data from HCSR-04 sensor but still, there is a good amount of precision. We can view the drawing process on the turtle screen below.

<img src="images/turtle_image1" height="250"> <img src="images/turtle_image2" height="250"> <img src="images/turtle_image3" height="250"> 


