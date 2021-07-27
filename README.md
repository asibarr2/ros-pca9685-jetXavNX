# ros-pca9685-jetXavNX
This is the PCA9685 package for the ROS Melodic using the Jetson Xavier NX using C++. All credit goes to Dheera for his work on https://github.com/dheera/ros-pwm-pca9685. This is a perfect package to be used with Donkey Car-esque projects.


### Pinout
In order to configure the package correctly, follow the correct pinout for wiring the PCA9685 to the Jetson Xavier NX. Here is a reference pinout for your convenience: https://www.jetsonhacks.com/nvidia-jetson-xavier-nx-gpio-header-pinout/

| Jetson Xavier NX | PCA9685 Adafruit |
|------------------|------------------|
| Pin 2 - 5.0V     |  VCC           |
| Pin 6 - GND      |   GND           |
| Pin 27 - SDA (I2C Bus 1) | SDA     |
| Pin 28 - SCL (I2C Bus 1) | SCL     |

Ensure that the pins above are wired correctly to the PCA9685. 

Most of the configuration for your PCA9685 will be located in **src/pca9685_activity.cpp** It is recommended to keep the default address at 0x40. 

### Change the frequency of Servo to 50 HZ
If you happen to have issues, go to **src/pca9685_activity.cpp** and change  

### Is your board being detected?
On the Jetson Xavier, your SDA and SCL pins will connected to Bus 1 of I2C. If you did not wire to the specified SDA/SCL pins above, your PCA9685 module will not work. To check if your address is being read, type in terminal:

  **sudo i2cdetect -r -y 1**

and you should see a 40 output in the following image: 
![alt text](https://github.com/asibarr2/[ros-pca9685-jetXavNX/pwm_pca9685/images/frequencyServo.png?raw=true)


If not, you need to check your wiring again.

To understand the parameters and setup, I will send you to this link: https://github.com/dheera/ros-pwm-pca9685 Dheera is the owner of the code and deserves credit, give him a follow as well if this helped you. 
