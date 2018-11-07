
SSD1306_OLED_Sensor
===============

### November 6th, 2018 (Week 10)

As outlined in my [project schedule](https://github.com/six0four/StudentSenseHat/blob/master/documentation/Week3RubricforProjectSchedule.xml), today is the PCB soldered milestone. With the completion of this milestone, I am within schedule with respect to the project completion. During the past week, I worked on creating the layout for PCB wiring and design in Fritzing. I aim to connect the SSD1306 OLED Monochrome display with the Raspberry Pi, and the sockets to enable this process were incorporated into the PCB design. I found [a site that offered hepful](https://www.raspberrypi-spy.co.uk/2018/04/i2c-oled-display-module-with-raspberry-pi/) information regarding connecting the pins and configuring the I2C interface, along with importing the relevant Python libraries. As outlined in my previous post, there was a problem detecting the address of the SSD1306 display. However, collaboration with Kelly and Vlad from the Prototype Lab helped to resolve the issue. That issue gave me an opportunity to delve deeper into troubleshooting hardware and sharpening my soldering skills. 

My [Budget](https://github.com/six0four/MicroRover/raw/master/PartsFor20MicroRoversRev02.xlsx) included headers, but these were not bought with the other products. Therefore, these [headers](https://www.digikey.ca/product-detail/en/sullins-connector-solutions/PPTC081LFBN-RC/S7006-ND/810147) were had from the Prototype Lab with a collective value of [$5.06](https://www.digikey.ca/product-detail/en/adafruit-industries-llc/2223/1528-1385-ND/5629433). My PCB design was done and Gerber files sent to the Protoype Lab for production without any problems. Here is an image of the [final PCB](https://github.com/six0four/StudentSenseHat/blob/master/electronics/StudentSenseHatV06.fzz) with soldered headers connected to the Rapberry pi and the [Fritzing files](jshgfojhsadf) that they result from. 


Week 9 PCB
---------------
This blog entry is to give a progress update on my hardware project. Last week there were some issues detecting the sensor's I2C address. However, after visiting Kelly and Vlad in the prototype lab during the course of the week we managed to find the problem and correct it. So at this time I am on track and within budget of my project. The PCB schema was designed and sent to the prototype lab for etching. I do not need to purchase any further part for the project so no additional cost is added to my original budget. Moving on to the soldering porting of the project next week.


Week 8 Hardware
-------------------
This blog entry is to give an update into my progress on my hardware sensor. At this point in the semester (Week 8), I am on schedule. However, I connected the SSD1306 OLED sensor using I2C connection but it did not work. I tried various times using various appropriate pin connectors but it still didn't work. The professor suggested tried connecting using SPI instead of I2C; or in case that didn't work, tried using an Arduino to see if that works. During the course of this week I will contact Vlad or Kelly at the prototype lab to figure out this problem. So this is a minor, or possibly a major setback in my progress. It will also put me in a negative financial status since I will have to repurchase the OLED sensor in the worst case scenario.

Image of what I have so far:
[Hardware Connection](hardware.png)


Week 7 Pseudocode Submission
-------------------------------


Week 6 
----------


Week 5 Proof of purchase
-------------
### Item(s) to be delivered
![Item(s) to be delivered this week](Index_src/oled_display.PNG)

### Item(s) already delivered
![Item(s) already delivered to recipient](Index_src/pi.png)

Week 4
---------------

Created [budget document](Documentation/Hardware_Production_Budget.xlsx)

Week 3
----------------

Created [Project Schedule](Documentation/Project_Schedule.mpp)

Week 2
---------------

Created [Proposal Content](Documentation/Proposal_Content.xlsx)

Created the GitHub repository
