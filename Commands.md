#Commands
- <a href=#section-check-os-version>Check OS verion on RPi</a>
- <a href=#section-reboot>Reboot</a>
- <a href=#section-shutdown>Shutdown</a>

<div id="section-check-os-version">
####Check OS version on RPi3

<b>cat /etc/os-release</b>
<pre>
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

####Service
<pre>
<b>service --status-all</b>            # <em>gives a list of services</em>
<b>service</b> <em>service-name</em>      # <em>gives further options for the command</em>
</pre>
