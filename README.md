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
9.  [Reproducible](#reproducible)

![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/stackable.png)

### Introduction
The aim of this project is to integrate a sensor/effector with the Broadcom development platform, also known as the Raspberry Pi, in order to read/write data to the device. The sensor/effector chosen for this project is the SSD1306 OLED Monochrome Display from Adafruit. It is a 1" diagonal display that is made of 128x64 individual white OLED pixels that uses both SPI and I2C interfaces. Over the course of fifteen weeks, few necessary documentations were created, including the project proposal, a project breakdown schedule, and budget for the project. The necessary hardware components were also acquired, along with the required components to put everything together. A wiring circuit diagram was developed in [Fritzing](http://fritzing.org/home/) and was used to breadboard and test the sensor with the Broadcom development platform. Using that prototype, a custom PCB was designed and sent to the Prototype lab for etching. Headers were then soldered to the PCB for stacking and final assembly. The image above demonstrate the final stackable interface for the project. 


### Bill of Materials
To embark on the project, the necessary parts and components will need to acquired. Displayed below is the budget of the price breakdown for components used in the project. The spreadsheet version of the budget with links to the sources for the components can be found [here](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/Documentation/Hardware_Production_Budget.xlsx).

![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/budget.PNG)

#### Listed below are some of the major components used in the project
SSD1306 OLED Monochrome 128x64 Display<br/>
![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/ssd1306.png)

Raspberry Pi Kit<br/>
![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/RasPiKit.png)

Components kit with stackable headers<br/>
![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/componentskit.png)


### Time Commitment
The entire project was done over the course of fifteen weeks, starting from selecting the OLED on September 4 to submitting the Build Instructions on December 11, 2018. However, to realistically build the project, a person could potentially use a weekend to complete it, assuming he has all the necessary components. Below is a breakdown of the project schedule.

![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/project_schedule.PNG)


### Mechanical Assembly
This step involves putting everything together. Hence, ensure the [8 pin header strip](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/ssd1306.png) that comes with the OLED display is securely soldered to the device. Ensure the [PCB](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/pcb.png) is designed in [Fritzing](http://fritzing.org/home/) and etched at the Prototype lab. Also, ensure the component [headers](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/componentskit.png) are soldered onto the PCB. The enclosure should also be designed in [CorelDraw](https://www.coreldraw.com/en/product/coreldraw/?topNav=en) and sent to the Prototype lab for lazer cutting. The final CorelDraw design for the enclosure can be found [here](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/Documentation/Pi2Case.cdr). After gathering all these components, now we are ready to assemble. Here are the steps involved: 

1. Mount the SSD1306 display to the PCB to create a stackable header<br/> 
![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/stackable.png)

2. Mount the stackable header to the Broadcom development platform GPIO port<br/>
![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/stackable2.png)

3. Install the Broadcom development platform with the stackable header in Acrylic enclosure<br/>
![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/PiEnclosure.png)


### PCB Soldering
Soldering the components will take a little effort especially if you have never soldered before. Some good lesson on soldering can be found [here](https://www.youtube.com/watch?v=oqV2xU1fee8). Here are the steps in soldering all the components for the project:

1. Solder the two jumpers on the back of the OLED. Both must be soldered 'closed' for the I2C interface to work.

![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/displays_oledi2c.png)

2. Solder the 8 pin header to the OLED display.

![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/header1.png)

3. Design the initial breadboard layout for the PCB in Fritzing

![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/SSD1306_BB_Wiring.png)

4. The breadboard design layout will automatically generate a schematic diagram for the PCB design 

![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/ssd1306_schema.png)

5. From the initial breadboard wiring design and resulting schema, design the actual PCB layout in Fritzing to send to production 

![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/SSD1306_Wiring_Final_pcb.png)

6. Image of the resulting etched PCB after production 

![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/pcb.png)

7. Below is an image of the headers soldered to the PCB with OLED display mounted

![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/stackabel1.png)

 8. Below is the stackable header mounting to the Broadcom development platform

![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/stackable2.png)


### Power Up
After connecting the OLED display with the Broadcom development platform through the I2C interface, the power up display looks like this:

![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/powerUpDisplay.png)


### Unit Testing
For the unit to be tested successfully, access to the internet is required as the SSD1306 Oled display will need the latest Python libraries and the Raspbian operating system will need to be up-to-date. Here are the steps involved in testing the unit:

1. Enable the I2C interface on the Raspberry pi. Run the following command and follow the steps:
  
       sudo raspi-config
   
![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/enable_i2c.png)
   
2. The second step is to ensure the I2C address is detected. To do that, execute the command: 

       sudo i2cdetect -y 1
    
The I2C address should look like this

![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/ssd1306_i2c_address.png)
    
3. Install the `RPi.GPIO` library by executing:

       sudo apt-get update
       sudo apt-get install build-essential python-dev python-pip
       sudo pip install RPi.GPIO `
     
4. Install the Python Imaging Library and smbus library by executing:
    
       sudo apt-get install python-imaging python-smbus
    
5. Download and install the SSD1306 python library code and examples, execute the following commands:

       sudo apt-get install git
       git clone https://github.com/adafruit/Adafruit_Python_SSD1306.git
       cd Adafruit_Python_SSD1306
       sudo python setup.py install `
    
6. Since we are using Raspbian operating system for this project, check the `/etc/modprobe.d/raspi-blacklist.conf` file and comment        `"blacklist i2c-bcm2708"` by running `sudo nano /etc/modprobe.d/raspi-blacklist.conf` and adding a `#` (if its not there).     

7. Navigate to the `Adafruit_Python_SSD1306/examples` subdirectory. You will find python scripts which demonstrate the usage of the        library. For example, open `shapes.py`. Comment `SSD1306_128_32` class and uncomment `SSD1306_128_64` class since we are using the      128x64 display. The default address used for the Python libraries is `3C`. However, the SSD1036 display uses the address `3D`. So add    the the code `i2c_bus_address=3D` after `rst=RST`. So the the class should look like this:

       disp = Adafruit_SSD1306.SSD1306_128_64(rst=RST, i2c_bus_address=3D) 
    
   You can run the code by executing this command in the examples directory: 
   
       sudo python shapes.py

   You should see something like this: 

![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/shapesDisplay.png)

   You have successfully integrated the Broadcom development platform with the SSD1306 Monochrome OLED display!


### Production Testing
Here is the display of the final product with all the components integrated. 

![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/PiEnclosure.png)


### Reproducible
Following this build instructions carefully will ensure the project is reproducible. 
