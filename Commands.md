#Commands
- <a href=#section-bluetoothctl>Bluetooth</a>
- <a href=#section-check-os-version>Check OS verion on RPi</a>
- <a href=#section-reboot>Reboot</a>
- <a href=#section-shutdown>Shutdown</a>
- <a href=#section-service>Service - check running services</a>

<div id="section-bluetoothctl">
####Bluetooth
<pre>
<b>bluetoothctl</b>

[NEW] Controller B8:27:EB:E6:18:F9 raspberrypi [default]
[bluetooth]#

[bluetooth]#<b> power on</b>
Changing power on succeeded
[bluetooth]#<b> scan on</b>
Discovery started
[CHG] Controller B8:27:EB:E6:18:F9 Discovering: yes
[NEW] Device F4:F9:51:D7:9A:3A F4-F9-51-D7-9A-3A
[CHG] Device F4:F9:51:D7:9A:3A RSSI: -91
[CHG] Device F4:F9:51:D7:9A:3A RSSI: -100
[CHG] Device F4:F9:51:D7:9A:3A RSSI: -90
[CHG] Device F4:F9:51:D7:9A:3A RSSI: -99
[CHG] Device F4:F9:51:D7:9A:3A RSSI: -90
[CHG] Device F4:F9:51:D7:9A:3A RSSI: -99
[NEW] Device 4E:D3:E1:A1:C5:A4 4E-D3-E1-A1-C5-A4
[CHG] Device F4:F9:51:D7:9A:3A RSSI: -89
[CHG] Device F4:F9:51:D7:9A:3A RSSI: -100
[CHG] Device F4:F9:51:D7:9A:3A RSSI: -90
[CHG] Device F4:F9:51:D7:9A:3A RSSI: -100
[CHG] Device F4:F9:51:D7:9A:3A RSSI: -91
[CHG] Device F4:F9:51:D7:9A:3A RSSI: -100
[CHG] Device F4:F9:51:D7:9A:3A RSSI: -90
[CHG] Device F4:F9:51:D7:9A:3A RSSI: -101
</pre>

<div id="section-check-os-version">
####Check OS version on RPi3

<pre>
<b>cat /etc/os-release</b>  # <em>look at the /etc/os-release file</em>

PRETTY_NAME="Raspbian GNU/Linux 8 (jessie)"
NAME="Raspbian GNU/Linux"
VERSION_ID="8"
VERSION="8 (jessie)"
ID=raspbian
ID_LIKE=debian
HOME_URL="http://www.raspbian.org/"
SUPPORT_URL="http://www.raspbian.org/RaspbianForums"
BUG_REPORT_URL="http://www.raspbian.org/RaspbianBugs"
</pre>

<div id="section-shutdown">
####Shutdown
<pre>
<b>sudo shutdown -s</b> <em>now</em>
</pre>

<div id="section-reboot">
####Reboot
<pre>
<b>sudo shutdown -r</b> <em>now</em>
</pre>

<div id="section-service">
####Service
<pre>
<b>service --status-all</b>            # <em>gives a list of services</em>
<b>service</b> <em>service-name</em>      # <em>gives further options for the service-name</em>
</pre>
