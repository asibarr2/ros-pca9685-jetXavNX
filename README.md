# ros-pca9685-jetXavNX
This is the PCA9685 package for the ROS Melodic using the Jetson Xavier NX using C++. All credit goes to Dheera for his work on https://github.com/dheera/ros-pwm-pca9685. This is a perfect package to be used with Donkey Car-esque projects.

In order to configure the package correctly, follow the correct pinout for wiring the PCA9685 to the Jetson Xavier NX. Here is a reference pinout for your convenience: https://www.jetsonhacks.com/nvidia-jetson-xavier-nx-gpio-header-pinout/

| Jetson Xavier NX | PCA9685 Adafruit |
---------------------------------------
| Pin 2 - 5.0V     |  VCC           |
| Pin 6 - GND      |   GND           |
| Pin 27 - SDA (I2C Bus 1) | SDA     |
| Pin 28 - SCL (I2C Bus 1) | SCL     |

| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |
