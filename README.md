# ESPHome-based doorbell with mute option in Home Assistant
The code is in deurbel.yaml, the only thing you need to change is your own wifi settings and, if desired, change some names.

The code is based on some personal preferences:
* Bell should not ring longer than 1 second (delay: 1000ms)
* Once presssed, you have to wait 5 seconds (delayed_off) AFTER releasing the button, before the bell will ring again. Pressing the button within 5 seconds will only reset the timer without ringing the bell.

In Home Assistant you'll need to create a boolean, which in my code is named "input_boolean.mute_doorbell". This piece of code is shown in home-assistant_input_boolean
