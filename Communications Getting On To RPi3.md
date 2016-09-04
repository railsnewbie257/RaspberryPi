###IP Scanner for Mac OS X
- found in the App Store  
- [also download here](http://10base-t.com/macintosh-software/ip-scanner/)

###Using VNC
To install VNC
<pre>
sudo apt-get install tightvncserver
</pre>

Then run VNC
<pre>
vncserver :1
</pre>

To check VNC is running
<pre>
ps -e | grep vnc
</pre>

Locking file for VNC is in `/tmp/.X1-lock`




###[Use-ssh-to-talk-with-your-Raspberry-Pi](http://www.instructables.com/id/Use-ssh-to-talk-with-your-Raspberry-Pi/)
On a Mac
<pre>
<b>ssh pi@</b><em>ip-address</em>
</pre>
You can find the <em>ip-address</em> by typing **ifconfig** on the RPI CLI.

###[how-to-tell-which-services-run-at-startup-on-raspberry-pi-raspbian](http://superuser.com/questions/852610/how-to-tell-which-services-run-at-startup-on-raspberry-pi-raspbian)

#VNC on RPi3
https://www.realvnc.com/docs/raspberry-pi.html

[RealVNC downloads](https://www.realvnc.com/download/vnc/?utm_medium=email&utm_campaign=license-emails&utm_source=free-trial-license&utm_content=download)

<em>download the VNC package</em>   
<b>curl -L -o VNC.tar.gz https://www.realvnc.com/download/binary/latest/debian/arm/ </b>
<pre>
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:--  0:00:01 --:--:--     0
100 12.0M  100 12.0M    0     0   612k      0  0:00:20  0:00:20 --:--:--  661k
</pre>

<em>get the package name</em>   
<b>tar xvf VNC.tar.gz</b>
<pre>
VNC-Server-5.3.2-Linux-ARM.deb
VNC-Viewer-5.3.2-Linux-ARM.deb
</pre>

<em>install package</em>   
<b>sudo dpkg -i VNC-Server-5.3.2-Linux-ARM.deb</b>
<pre>
(Reading database ... 119726 files and directories currently installed.)
Preparing to unpack VNC-Server-5.3.2-Linux-ARM.deb ...
Unpacking realvnc-vnc-server (5.3.2.19179) ...
Setting up realvnc-vnc-server (5.3.2.19179) ...
Updating /etc/pam.d/vncserver
Updating /etc/pam.conf... done
Looking for font path... not found.
Generating private key... done
Installed systemd unit for VNC Server in Service Mode daemon
Start or stop the service with:
  systemctl (start|stop) vncserver-x11-serviced.service
Mark or unmark the service to be started at boot time with:
  systemctl (enable|disable) vncserver-x11-serviced.service

Installed systemd unit for VNC Server in Virtual Mode daemon
Start or stop the service with:
  systemctl (start|stop) vncserver-virtuald.service
Mark or unmark the service to be started at boot time with:
  systemctl (enable|disable) vncserver-virtuald.service


(gconftool-2:4503): GConf-WARNING **: Client failed to connect to the D-BUS daemon:
Unable to autolaunch a dbus-daemon without a $DISPLAY for X11
gconfd-2: no process found
Processing triggers for gconf2 (3.2.6-3) ...
Processing triggers for hicolor-icon-theme (0.13-1) ...
Processing triggers for man-db (2.7.0.2-5) ...
Processing triggers for shared-mime-info (1.3-1) ...
Processing triggers for gnome-menus (3.13.3-6) ...
Processing triggers for desktop-file-utils (0.22-1) ...
Processing triggers for mime-support (3.58) ...
</pre>
<em>add license key</em>   
<b>sudo vnclicense -add</b> <em>license-key</em>
<pre>
License key &lt;Free&gt; has been successfully applied.
</pre>
