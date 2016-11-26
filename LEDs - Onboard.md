https://www.raspberrypi.org/forums/viewtopic.php?f=31&t=12530

The green OK LED can be controlled from software. It's available as /sys/class/leds/led0/

The kernel LED driver, which controls led0, has "triggers" which let some other part of the kernel control the LED.   
The default trigger for the LED is 'mmc0', which makes it come on when the SD card is accessed.

root@raspberrypi:~# cat /sys/class/leds/led0/trigger   
none [mmc0]

Here, the **mmc0** trigger is selected. You can deactivate this as follows:
<pre>
$ <b>echo none >/sys/class/leds/led0/trigger</b>
</pre>
The LED can be turned on and off using the **'brightness' file**.  
The minimum brightness is 0, and the maximum is 255 (specified in the 'max_brightness' file).   
However, as there is no hardware support for variable brightness, any value greater than 0 will turn the LED on.
<pre>
$ <b>echo 1 >/sys/class/leds/led0/brightness</b>   
$ <b>echo 0 >/sys/class/leds/led0/brightness</b>
</pre>
Setting the brightness to 0 automatically sets the trigger to "none"

If you want the LED to go back to its default function:
<pre>
$ <b>echo mmc0 >/sys/class/leds/led0/trigger</b>
</pre>
As an aside, there are a couple of kernel modules you can load up (`ledtrig_timer` and `ledtrig_heartbeat`) which will flash the LED for you.
<pre>
$ <b>modprobe ledtrig_heartbeat</b>
$ <b>echo heartbeat >/sys/class/leds/led0/trigger</b>
</pre>
Once you have turned off the **mmc0** trigger, you can use **GPIO16** to control the LED.   
It's **active-low**, so you need to set the pin low to turn the LED on, and high to turn it off.

Sample code, using http://pypi.python.org/pypi/RPi.GPIO

<pre>
#!/usr/bin/python

import RPi.GPIO as GPIO
from time import sleep

# Needs to be BCM. GPIO.BOARD lets you address GPIO ports by periperal
# connector pin number, and the LED GPIO isn't on the connector
GPIO.setmode(GPIO.BCM)

# set up GPIO output channel
GPIO.setup(16, GPIO.OUT)

# On
GPIO.output(16, GPIO.LOW)

# Wait a bit
sleep(10)

# Off
GPIO.output(16, GPIO.HIGH)
</pre>

It's important to note that RPi.GPIO will set the GPIO port to be an input when it's finished (it sets to an input any port which the script set to an output, and you have to set it to an output before you can do anything with it, even if it already was). As GPIO16 stops being an output, control via the kernel interface will no longer work.
