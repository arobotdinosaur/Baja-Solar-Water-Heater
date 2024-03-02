This is the controller for a solar powered water heater that runs at La Hacienda de la Inmaculada in Tijuana. It is designed to run on an ESP32-S3 board. The code was mostly written by Darell Chua, but Alexander Haken made a few changes. More documentation to come, I promise!

The general logic behind the pump controller is that the pump runs whenever 2 criteria are true: The water heater must be below its target temperature (currently set to 50 degrees celcius), and the solar heating panel on the roof must be at least 10 degrees celsius warmer than the water heater. 
Darell's github:
https://github.com/darrll27/Baja-Solar-ENG-100L/tree/main/ESP32_Baja_Solar_Wifi
