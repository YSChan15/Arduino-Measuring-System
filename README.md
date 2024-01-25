# Arduino Nano code 

## Before you start 

### Program / hardware needed 

- Arduino IDE 
>Install Arduino IDE from this [link](https://downloads.arduino.cc/arduino-1.8.19-windows.exe).

> **NOTE** : This code is programmed using Arduino IDE 1.8.19, which is a Legacy IDE.

- Mini-B USB cable 

### Libraries

#### Library of DFROBOT_QMC5883
* Download the included zip libraries or go to [DFRobot Link](https://github.com/DFRobot/DFRobot_QMC5883) to download the zip folder

* To include the libraries, go to Sketch -> Include Library -> Add ZIP Library and add your downloaded library

* Use #include <DFRobot_QMC5883.h> as your header file


#### Library of MPU6050_light
* To include the libraries, go to Sketch -> Include Library -> Manage Library

* Search for MPU6050_light by rfetick and click install

* Use #include <MPU6050_light.h> as your header file


#### Library of GT-U7 GPS module
* To include the libraries, go to Sketch -> Include Library -> Manage Library

* Search for TinyGPSPlus by Mikah Hart and click install

* Use #include <TinyGPS++.h> as your header file


**NOTE FOR GPS Module Connection**

> * To get a good and stable GPS connection, it is best to use the system outdoors / close to window.
>
> * Use your OWN location. Find it via [Magnetic Declination Website](http://magnetic-declination.com/) to get your inclination or declination angle.
> 
> * Replace your angle at the following line:
>
>  **For example:**
>
>  **float declinationAngle = (X + (Y / 60.0)) / (180 / PI);**
>
>  **St Cloud / Waite Park Angle = 0'38E**
>
>  
>  ***Replace X and Y with the following angle above***
>
>  
>  **float declinationAngle = (0 + (38.0 / 60.0)) / (180 / PI);**

## Programming / Debugging the Arduino Nano

* Remove the BLE module first before you program the Arduino Nano.
> If Arduino is not being reprogrammed, there's no need to remove the BLE module.

* If Arduino errors out during the upload, check if the board used is correct. Make sure the board selected is correct (In this case its Arduino Nano).
> Change the processor to the one with "old bootloader" in its name if it does not program.  

* Make sure the lights on GPS, MPU6050 gyroscopic sensor, and LiDAR module are getting powered (indicated by the LED's).

* Calibrate the compass sensor by turning the entire system 360 degrees. 

* Use the Serial Monitor to observe the data being collected. If data(distance) measured is not consistent when being left idle, reseat the LiDAR cable.


## Purchase link 
Purchase link can be found below if replacement part is needed. 

[**GPS SENSOR**](https://www.amazon.com/Navigation-Satellite-Compatible-Microcontroller-Geekstory/dp/B07PRGBLX7?th=1)

[**BLE module**](https://www.amazon.com/DSD-TECH-Bluetooth-iBeacon-Arduino/dp/B06WGZB2N4)

[**MPU 6050**](https://www.amazon.com/HiLetgo-MPU-6050-Accelerometer-Gyroscope-Converter/dp/B01DK83ZYQ/ref=asc_df_B01DK83ZYQ/?tag=hyprod-20&linkCode=df0&hvadid=642109977814&hvpos=&hvnetw=g&hvrand=8430803264096386904&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=1020086&hvtargid=pla-1260970162741&gclid=EAIaIQobChMI7fH7s9OPggMV_1J_AB3O2gLQEAQYASABEgKCrPD_BwE&th=1)

[**HMC 5883**](https://amazon.com/HiLetgo-GY-271-QMC5883L-Compass-Magnetometer/dp/B008V9S64E/ref=asc_df_B008V9S64E/?tag=hyprod-20&linkCode=df0&hvadid=241933244562&hvpos=&hvnetw=g&hvrand=4729607995161709394&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=1020086&hvtargid=pla-650173234261&psc=1)

[**Arduino NANO Microcontroller**](https://store.arduino.cc/products/arduino-nano)

[**SF11/C LiDAR Sensor**](https://www.mouser.com/ProductDetail/LightWare-LiDAR/SF11-C?qs=iLbezkQI%252BsjRfbQfbtoV7g%3D%3D&mgh=1&gad_source=1&gclid=EAIaIQobChMIi9Sq6PL3gwMVoVdHAR0QQQRgEAQYAiABEgKM2_D_BwE)
