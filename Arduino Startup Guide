Written by Alexander Haken on 2/20/2024
Email alexand@sonic.net with any questions

Notes/Primitive Guide on getting set up with the esp32-S3 board that is used in the pump controller 

Darell’s code that runs on the board:
https://github.com/darrll27/Baja-Solar-ENG-100L/blob/main/ESP32_Baja_Solar_Wifi/ESP32_Baja_Solar_Wifi.ino 

Alexander’s GitHub with an edited version of the code:
https://github.com/arobotdinosaur/Baja-Solar-Water-Heater 

https://docs.espressif.com/projects/arduino-esp32/en/latest/installing.html 
Read these instructions for using the Arduino IDE to set up the esp32, you’ll have to manually add the following libraries in the Arduino side panel to get the program to compile successfully.

 #include <Wire.h>
#include <Adafruit_GFX.h>
#include <Adafruit_SSD1306.h>
#include <OneWire.h>
#include <DallasTemperature.h>
#include <WiFi.h>
#include <WebServer.h>

The esp32-S3 board has 2 USB-C ports, one labeled “comm,” and one labeled “USB.” Use the USB one for flashing programs to the esp32, and the comm for receiving communications from the board. 

Plug the board into the USB port, save Darell’s code from the GitHub above as a new file, then compile it and upload it to the esp32-S3 (buttons in the upper left corner).

Once the code is updated, you should see the wifi Baja_Solar_pw00000000 pop-up, the password is 00000000. 

To receive communications from the board, plug in a second USB cable to the comm port and connect to it in the Arduino IDE. Make sure to use 115200 as the baud rate for communication. You should see the thermocouple temperatures being logged, as well as the flow rate.

To connect to a website that displays the thermocouple data and flow meter data, go to http://192.168.4.1/ in a web browser while you’re connected to the ESP32 generated wifi network.

Darell’s GitHub has a program called Baja_Solar_Wifi_Logger.py, if you run this while connected to the esp32 wifi network it makes a nice spreadsheet of all the data about the thermocouples and the pump. If you are on a Mac/windows you should be able to just run the program without installing anything by typing “python Baja_Solar_Wifi_Logger.py” or “python3 Baja_Solar_Wifi_Logger.py,” in your terminal/PowerShell. If for some reason python wasn’t pre-installed there are many different ways to install it.

Note: If you prefer command line tools to the Arduino IDE, there is also a command line development kit with instructions here: https://docs.espressif.com/projects/esp-idf/en/stable/esp32/get-started/ 
I haven’t tried it yet but it should work just as well.

The esp32 just launches the Baja controls program immediately on startup and keeps running it forever. 



