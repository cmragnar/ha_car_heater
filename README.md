First, Go support kotope as he is the original developer of the package.
https://github.com/kotope
Big thanks to him!

## Car heater automation package for Home Assistant.
Automated car heater package for Home Assistant to pre-heat your car at specified departure time.
Requirements: Home Assistant and HA supported plug with energy consumption measurement.


#Car Heater Automation for Home Assistant
##Description

**This automation controls a car engine heater based on outdoor temperature and a scheduled departure time. It ensures the car is warm when needed while optimizing energy usage.**

- Automatically starts the heater at a calculated time before departure.
- Prevents overheating by enforcing a max runtime of 3 hours.
- Sends a notification if the heater turns on but no power is detected (cable unplugged).
- Works only on weekdays if enabled via input_boolean.car_heater_weekday.
- Samples temperature 3 hours before departure to calculate required heating time.
