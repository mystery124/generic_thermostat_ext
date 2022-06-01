# GENERIC THERMOSTAT EXTENSION
This component is a revision of the official Home Assistant component 'Generic Thermostat' in order to have possibility to have multiple heaters.

## EXAMPLE OF SETUP
Config flow is available, so just configure all the entities you want through the user interface.

Here below the example of manual setup of sensor and parameters to configure.
```yaml
- platform: generic_thermostat_ext
  name: Kitchen
  heater: switch.heating_kitchen
  heaters_related:
    - switch.heating_dining_room
  target_sensor: sensor.kitchen_temp_temperature
  min_temp: 15
  max_temp: 28
  cold_tolerance: 0.2
  hot_tolerance: 0.2
  target_temp_step: 0.1
  away_temp: 20.0
  home_temp: 22.0
  sleep_temp: 20.5
  comfort_temp : 25.0
  precision : 0.1
  min_cycle_duration: 00:05:00
  keep_alive: 00:01:00
```