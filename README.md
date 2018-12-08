# SSD1306-monochrome-OLED

## Built Instruction for Broadcom Devepolment Platform (Raspberry Pi 3B+) and SSD1306 OLED Display

### Table of Contents
1. [Introduction](#introduction)
2. [Bill of Materials](#bill-of-materials) 
3. [Time Commitment](#time-commitment)
4. [Mechanical Assembly](#mechanical-assembly)
5. [PCB/Soldering](#pcb-/-soldering)
6. [Power Up](#power-up)
7. [Unit Testing](#unit-testing)
8. [Production Testing](#production-testing)

![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/stackable.jpg)

### Introduction
The aim of this hardware project is to integrate a sensor/effector with the Broadcom development platform, also known as the Raspberry Pi, in order to read/write data to the device. The sensor/effecor I have chosen for this project is the SSD1306 OLED Monochrome Display from Adafruit. It is a 1" diagonal display that is made of 128X64 individual white OLED pixels that uses both SPI and I2C interfaces. Over the course of fifteen weeks I have created the project proposal, a project breakdown schedule, a budget for the project, and have acquired the hardware devices anong with the components to put them together. I have also breadboarded a circuit to test my sensor with the development platform using Fritzing. Using that design, I created a custom PCB for laser etching, then soldered the acquired components to the PCB for final assembly. The image above is the final stackable interface for the project. 

### Bill of Materials
Below is the budget of the entire project along with a link to the sources of the materials. The exel file can be downloaded [here](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/Documentation/Hardware_Production_Budget.xlsx)
![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/budget.PNG)

### Some of the major components of the project. 
![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/ssd1306.jpg)
![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/componentskit.jpg)
![]()
![]()

### Time Commitment
This entire project was done over the course of fifteen weeks, starting from selecting my OLED on September 4 to submitting my Build Instructions on December 11, 2018. Below is a breakdown of the schedule.
![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/project_schedule.PNG)

### Mechanical Assembly
Below is a list of the stages of mechanical assemply of the project.
![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/pcb.jpg)
![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/Index_src/pcbwithheaders1.jpg)
![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/images/stackable.jpg)
![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/Index_src/stackable1.jpg)
![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/Index_src/PiCase.jpg)

### PCB/Soldering
Below is a image of the PCB with soldered headers for mounting the Broadcom development platform and OLED display.
![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/Index_src/pcb.jpg)
![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/Index_src/pcbwithheaders1.jpg)

### Power Up
After connecting the OLED display with the Broadcom development platform through the I2C interface, the power up display look like this:
![](https://github.com/dchristie75/SSD1306-Monochrome-OLED/blob/master/Index_src/20181113_000239.jpg)

### Unit Testing


### Production Testing

