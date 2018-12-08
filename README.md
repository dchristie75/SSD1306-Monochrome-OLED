# SSD1306 Monochrome OLED

## Build Instructions for Broadcom Devepolment Platform (Raspberry Pi 3B+) and SSD1306 OLED Display

### Table of Contents
1.  [Introduction](#introduction)
2.  [Bill of Materials](#bill-of-materials) 
3.  [Time Commitment](#time-commitment)
4.  [Mechanical Assembly](#mechanical-assembly)
5.  [PCB/Soldering](#pcb-soldering)
6.  [Power Up](#power-up)
7.  [Unit Testing](#unit-testing)
8.  [Production Testing](#production-testing)

![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/stackable.jpg)

### Introduction
The aim of this hardware project is to integrate a sensor/effector with the Broadcom development platform, also known as the Raspberry Pi, in order to read/write data to the device. The sensor/effecor I have chosen for this project is the SSD1306 OLED Monochrome Display from Adafruit. It is a 1" diagonal display that is made of 128X64 individual white OLED pixels that uses both SPI and I2C interfaces. Over the course of fifteen weeks I have created the project proposal, a project breakdown schedule, a budget for the project, and have acquired the hardware devices anong with the components to put them together. I have also breadboarded a circuit to test my sensor with the development platform using Fritzing. Using that design, I created a custom PCB for laser etching, then soldered the acquired components to the PCB for final assembly. The image above is the final stackable interface for the project. 


### Bill of Materials
Below is the budget of the entire project along with a link to the sources of the materials. The exel file can be downloaded [here](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/Documentation/Hardware_Production_Budget.xlsx).

![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/budget.PNG)

### Major components of the project
SSD1306 OLED Monochrome 128x64 Display
![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/ssd1306.jpg)
Components kit with stackable headers
![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/componentskit.jpg)
![]()
![]()

### Time Commitment
This entire project was done over the course of fifteen weeks, starting from selecting my OLED on September 4 to submitting my Build Instructions on December 11, 2018. Below is a breakdown of the schedule.

![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/project_schedule.PNG)


### Mechanical Assembly
PCB design
![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/pcb.jpg)
PCB with soldered stackable headers
![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/Index_src/pcbwithheaders1.jpg)
SSD1306 display mounted to the PCB 
![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/stackable.jpg)
Stackable headers with OLED display mounted to the Broadcom development platform
![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/Index_src/stackable1.jpg)
Final product enclosed in Acrylic case
![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/Index_src/PiCase.jpg)

### PCB Soldering
Below is a image of the PCB with soldered headers for mounting the Broadcom development platform and OLED display.

![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/Index_src/pcb.jpg)
![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/Index_src/pcbwithheaders1.jpg)

### Power Up
After connecting the OLED display with the Broadcom development platform through the I2C interface, the power up display look like this:

![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/Index_src/20181113_000239.jpg)


### Unit Testing
Ensure you can detect the I2C interface by executing the command:

    sudo i2cdetect -y 1
    
The I2C address should look like this

![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/ssd1306_i2c_address.png)
    
Install the `RPi.GPIO` library by executing:

    sudo apt-get update
    sudo apt-get install build-essential python-dev python-pip
    sudo pip install RPi.GPIO
    
Install the Python Imaging Library and smbus library by executing:

    sudo apt-get install python-imaging python-smbus

Download and install the SSD1306 python library code and examples, execute the following commands:

    sudo apt-get install git
    git clone https://github.com/adafruit/Adafruit_Python_SSD1306.git
    cd Adafruit_Python_SSD1306
    sudo python setup.py install
    
Since for this project we are using Raspbian, check the `/etc/modprobe.d/raspi-blacklist.conf` file and comment `"blacklist i2c-bcm2708"` by running `sudo nano /etc/modprobe.d/raspi-blacklist.conf` and adding a `#` (if its not there).     

#### Usage
Inside the `Adafruit_Python_SSD1306/examples` subdirectory are python scripts which demonstrate the usage of the library. For example, open `shapes.py`. Comment SSD1306_128_32 class and uncomment SSD1306_128_64 class. Add the the code `i2c_bus_address=3D` after rst=RST. So the the class should look like this:

    disp = Adafruit_SSD1306.SSD1306_128_64(rst=RST, i2c_bus_address=3D)
    
You can run the code by executing this command in the examples directory:

    sudo python shapes.py

You should see something like this: 
![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/shapes.jpg)


### Production Testing

