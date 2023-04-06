# Transient-Switch-Home-Assistant
This is a custom integration for Home Assistant that creates a switch that automatically turns off after a specified time interval. The switch can be configured to count the number of times it has been turned on and off within a certain interval and can optionally restore its previous state after the interval has elapsed.

To add this integration to Home Assistant, create a new folder named "transient_switch" in the "/config/custom_components/" directory and copy the three files listed below into that folder:

init.py
manifest.json
switch.py

Then, add the following configuration to your Home Assistant configuration.yaml file:

```
switch:
  - platform: transient_switch
    name: My Transient Switch
    interval_start: "09:00:00"
    interval_end: "17:00:00"
```    
    
Replace "My Transient Switch" with a name of your choice and set the "interval_start" and "interval_end" times to the desired start and end times of the interval when the switch should be turned on. Other optional configuration parameters can be added as well, as described in the comments of the "switch.py" file.

After configuring the switch, it can be added to Home Assistant entities as any other switch. The switch will turn off automatically after the specified interval has elapsed.
