#Commands

####Check OS version on RPi3
<pre>
<b>cat /etc/os-release</b>

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


####Shutdown
<pre>
<b>sudo shutdown -s</b> <em>now</em>
</pre>

####Reboot
<pre>
<b>sudo shutdown -r</b> <em>now</em>
</pre>

####Service
<pre>
<b>service --status-all</b>            # <em>gives a list of services</em>
<b>service</b> <em>service-name</em>      # <em>gives further options for the command</em>
</pre>
