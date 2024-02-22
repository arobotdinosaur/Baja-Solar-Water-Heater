This is the controller for a solar powered water heater that runs at La Hacienda de la Inmaculada in Tijuana. It is designed to run on an ESP32-S3 board. The code was mostly written by Darell Chua, but Alexander Haken made a few changes. More documentation to come, I promise!

The general logic behind the pump controller is that the runs whenever 2 criteria are true: The water heater must be below its target temperature, and the solar heating panel on the roof must be at least 1 degree celsius warmer than the water heater. Furthermore, to ensure that the thermocouples are giving accurate readings, the pump is turned on for 30 seconds every 30 minutes. This is because the thermocouples are not actually in the water heater/solar heating panel but rather in pipes near the outlets of those two systems.

Darell's github:
https://github.com/darrll27/Baja-Solar-ENG-100L/tree/main/ESP32_Baja_Solar_Wifi
