# ESPHome-based doorbell with mute option in Home Assistant
The code is in deurbel.yaml, the only thing you need to change is your own wifi settings and, if desired, change some names.

The code is based on some personal preferences:
* Bell should not ring longer than 1 second (delay: 1000ms)
* Once presssed, you have to wait 5 seconds (delayed_off) AFTER releasing the button, before the bell will ring again. Pressing the button within 5 seconds will only reset the timer without ringing the bell.

In Home Assistant you'll need to create a boolean, which in my code is named "input_boolean.mute_doorbell". This piece of code is shown in home-assistant_input_boolean
# The hardware
The hardware is quite easy. It's based on a Wemos D1 mini. That's powered on the 5V pin. The doorbell is connected between the 3.3V and the D2 connector. There is a resistor between ground and D2 (this can be anything between 1K and 100K, I've used a 1K here) for a pull-down to ground. So D2 is always low (via the resistor), until the doorbell is presssed, than it's high (3.3V).

The D1 is directly connected to the Wemos Relay shield (bought mine via Aliexpress, If you've got another one which requires another connector, change the code for that).
