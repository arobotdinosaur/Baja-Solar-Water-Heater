This is the controller for a solar powered water heater that runs at Casa Hogar de Maria Inmaculada in Tijuana. It is designed to run on an ESP32-S3 board. The code was mostly written by Darell Chua, but Alexander Haken made a few changes. More documentation to come, I promise!

The general logic behind the pump controller is that the pump runs whenever 2 criteria are true: The water heater must be below its target temperature (currently set to 50 degrees celsius), and the solar heating panel on the roof must be at least 10 degrees celsius warmer than the water heater. Once the pump is on, it will not turn off until the roof temperature falls to be 7 degrees celsius warmer than the water heater (or the water heater temperature raises to be within 7 degrees of the roof).

The code also shuts down the pump and outputs an error code if any thermocouple ever reads below O degrees celsius or above 95 degrees celsius.
