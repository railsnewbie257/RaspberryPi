<pre>
<b>systemctl status bluetooth</b>
</pre>

[Headless Bluetooth Pairing](https://www.raspberrypi.org/forums/viewtopic.php?t=53299&p=409980)

[hcitool commands](http://www.tutorialspoint.com/unix_commands/hcitool.htm)

[Setting up Bluetooth on the Raspberry Pi 3](https://www.element14.com/community/docs/DOC-81266/l/setting-up-bluetooth-on-the-raspberry-pi-3)

####Bluetooth Installation
<pre>
<b>sudo apt-get install bluetooth bluez blueman</b>

Reading package lists... Done
Building dependency tree       
Reading state information... Done
bluez is already the newest version.
bluez set to manually installed.
The following extra packages will be installed:
  fonts-droid ghostscript gir1.2-appindicator3-0.1 gir1.2-gconf-2.0 gir1.2-notify-0.7 imagemagick-common
  indicator-application libappindicator3-1 libdbusmenu-glib4 libdbusmenu-gtk3-4 libgs9 libgs9-common libijs-0.35
  libindicator3-7 libjbig2dec0 liblqr-1-0 libmagickcore-6.q16-2 libmagickwand-6.q16-2 libopenobex1 libpaper-utils
  libpaper1 libpulse-mainloop-glib0 notification-daemon obex-data-server python-gi-cairo
Suggested packages:
  bluez-cups bluez-obexd ghostscript-x libmagickcore-6.q16-2-extra
The following NEW packages will be installed:
  blueman bluetooth fonts-droid ghostscript gir1.2-appindicator3-0.1 gir1.2-gconf-2.0 gir1.2-notify-0.7
  imagemagick-common indicator-application libappindicator3-1 libdbusmenu-glib4 libdbusmenu-gtk3-4 libgs9
  libgs9-common libijs-0.35 libindicator3-7 libjbig2dec0 liblqr-1-0 libmagickcore-6.q16-2 libmagickwand-6.q16-2
  libopenobex1 libpaper-utils libpaper1 libpulse-mainloop-glib0 notification-daemon obex-data-server python-gi-cairo
0 upgraded, 27 newly installed, 0 to remove and 10 not upgraded.
Need to get 12.5 MB of archives.
After this operation, 41.8 MB of additional disk space will be used.
Do you want to continue? [Y/n] <b>Y</b>
Get:1 http://archive.raspberrypi.org/debian/ jessie/ui fonts-droid all 1:4.4.4r2-6+rpi1 [3,728 kB]
Get:2 http://mirrordirector.raspbian.org/raspbian/ jessie/main imagemagick-common all 8:6.8.9.9-5+deb8u3 [150 kB]      
Get:3 http://mirrordirector.raspbian.org/raspbian/ jessie/main libdbusmenu-glib4 armhf 12.10.2-1 [95.6 kB]             
Get:4 http://mirrordirector.raspbian.org/raspbian/ jessie/main libdbusmenu-gtk3-4 armhf 12.10.2-1 [85.2 kB]            
Get:5 http://mirrordirector.raspbian.org/raspbian/ jessie/main libijs-0.35 armhf 0.35-10 [18.5 kB]                     
Get:6 http://mirrordirector.raspbian.org/raspbian/ jessie/main liblqr-1-0 armhf 0.4.2-2 [20.9 kB]                      
Get:7 http://mirrordirector.raspbian.org/raspbian/ jessie/main libpaper1 armhf 1.1.24+nmu4 [21.4 kB]                   
Get:8 http://mirrordirector.raspbian.org/raspbian/ jessie/main libpulse-mainloop-glib0 armhf 5.0-13 [28.5 kB]          
Get:9 http://mirrordirector.raspbian.org/raspbian/ jessie/main libopenobex1 armhf 1.5-2.1 [21.3 kB]                    
Get:10 http://mirrordirector.raspbian.org/raspbian/ jessie/main notification-daemon armhf 0.7.6-2 [48.9 kB]            
Get:11 http://mirrordirector.raspbian.org/raspbian/ jessie/main gir1.2-notify-0.7 armhf 0.7.6-2 [19.8 kB]              
Get:12 http://mirrordirector.raspbian.org/raspbian/ jessie/main python-gi-cairo armhf 3.14.0-1 [310 kB]                
Get:13 http://mirrordirector.raspbian.org/raspbian/ jessie/main libindicator3-7 armhf 0.5.0-2 [48.9 kB]                
Get:14 http://mirrordirector.raspbian.org/raspbian/ jessie/main libmagickcore-6.q16-2 armhf 8:6.8.9.9-5+deb8u3 [1,526 kB]
Get:15 http://mirrordirector.raspbian.org/raspbian/ jessie/main libappindicator3-1 armhf 0.4.92-3.1 [50.0 kB]          
Get:16 http://mirrordirector.raspbian.org/raspbian/ jessie/main gir1.2-appindicator3-0.1 armhf 0.4.92-3.1 [38.3 kB]    
Get:17 http://mirrordirector.raspbian.org/raspbian/ jessie/main gir1.2-gconf-2.0 armhf 3.2.6-3 [362 kB]                
Get:18 http://mirrordirector.raspbian.org/raspbian/ jessie/main libjbig2dec0 armhf 0.11+20120125-1 [46.4 kB]           
Get:19 http://mirrordirector.raspbian.org/raspbian/ jessie/main indicator-application armhf 0.5.0-1 [57.5 kB]          
Get:20 http://mirrordirector.raspbian.org/raspbian/ jessie/main libpaper-utils armhf 1.1.24+nmu4 [17.2 kB]             
Get:21 http://archive.raspberrypi.org/debian/ jessie/main bluetooth all 5.23-2+rpi2 [36.5 kB]                          
Get:22 http://mirrordirector.raspbian.org/raspbian/ jessie/main libmagickwand-6.q16-2 armhf 8:6.8.9.9-5+deb8u3 [382 kB]
Get:23 http://mirrordirector.raspbian.org/raspbian/ jessie/main obex-data-server armhf 0.4.5-1+b3 [76.4 kB]            
Get:24 http://mirrordirector.raspbian.org/raspbian/ jessie/main blueman armhf 1.99~alpha1-1+deb8u1 [1,687 kB]          
Get:25 http://mirrordirector.raspbian.org/raspbian/ jessie/main libgs9-common all 9.06~dfsg-2+deb8u1 [1,979 kB]        
Get:26 http://mirrordirector.raspbian.org/raspbian/ jessie/main libgs9 armhf 9.06~dfsg-2+deb8u1 [1,603 kB]             
Get:27 http://mirrordirector.raspbian.org/raspbian/ jessie/main ghostscript armhf 9.06~dfsg-2+deb8u1 [83.2 kB]         
Fetched 12.5 MB in 5min 2s (41.5 kB/s)      
Preconfiguring packages ...
Selecting previously unselected package fonts-droid.
(Reading database ... 119746 files and directories currently installed.)
Preparing to unpack .../fonts-droid_1%3a4.4.4r2-6+rpi1_all.deb ...
Unpacking fonts-droid (1:4.4.4r2-6+rpi1) ...
Selecting previously unselected package imagemagick-common.
Preparing to unpack .../imagemagick-common_8%3a6.8.9.9-5+deb8u3_all.deb ...
Unpacking imagemagick-common (8:6.8.9.9-5+deb8u3) ...
Selecting previously unselected package libdbusmenu-glib4:armhf.
Preparing to unpack .../libdbusmenu-glib4_12.10.2-1_armhf.deb ...
Unpacking libdbusmenu-glib4:armhf (12.10.2-1) ...
Selecting previously unselected package libdbusmenu-gtk3-4:armhf.
Preparing to unpack .../libdbusmenu-gtk3-4_12.10.2-1_armhf.deb ...
Unpacking libdbusmenu-gtk3-4:armhf (12.10.2-1) ...
Selecting previously unselected package libijs-0.35:armhf.
Preparing to unpack .../libijs-0.35_0.35-10_armhf.deb ...
Unpacking libijs-0.35:armhf (0.35-10) ...
Selecting previously unselected package liblqr-1-0:armhf.
Preparing to unpack .../liblqr-1-0_0.4.2-2_armhf.deb ...
Unpacking liblqr-1-0:armhf (0.4.2-2) ...
Selecting previously unselected package libmagickcore-6.q16-2:armhf.
Preparing to unpack .../libmagickcore-6.q16-2_8%3a6.8.9.9-5+deb8u3_armhf.deb ...
Unpacking libmagickcore-6.q16-2:armhf (8:6.8.9.9-5+deb8u3) ...
Selecting previously unselected package libmagickwand-6.q16-2:armhf.
Preparing to unpack .../libmagickwand-6.q16-2_8%3a6.8.9.9-5+deb8u3_armhf.deb ...
Unpacking libmagickwand-6.q16-2:armhf (8:6.8.9.9-5+deb8u3) ...
Selecting previously unselected package libpaper1:armhf.
Preparing to unpack .../libpaper1_1.1.24+nmu4_armhf.deb ...
Unpacking libpaper1:armhf (1.1.24+nmu4) ...
Selecting previously unselected package libpulse-mainloop-glib0:armhf.
Preparing to unpack .../libpulse-mainloop-glib0_5.0-13_armhf.deb ...
Unpacking libpulse-mainloop-glib0:armhf (5.0-13) ...
Selecting previously unselected package libopenobex1.
Preparing to unpack .../libopenobex1_1.5-2.1_armhf.deb ...
Unpacking libopenobex1 (1.5-2.1) ...
Selecting previously unselected package obex-data-server.
Preparing to unpack .../obex-data-server_0.4.5-1+b3_armhf.deb ...
Unpacking obex-data-server (0.4.5-1+b3) ...
Selecting previously unselected package notification-daemon.
Preparing to unpack .../notification-daemon_0.7.6-2_armhf.deb ...
Unpacking notification-daemon (0.7.6-2) ...
Selecting previously unselected package gir1.2-notify-0.7.
Preparing to unpack .../gir1.2-notify-0.7_0.7.6-2_armhf.deb ...
Unpacking gir1.2-notify-0.7 (0.7.6-2) ...
Selecting previously unselected package python-gi-cairo.
Preparing to unpack .../python-gi-cairo_3.14.0-1_armhf.deb ...
Unpacking python-gi-cairo (3.14.0-1) ...
Selecting previously unselected package libindicator3-7.
Preparing to unpack .../libindicator3-7_0.5.0-2_armhf.deb ...
Unpacking libindicator3-7 (0.5.0-2) ...
Selecting previously unselected package libappindicator3-1.
Preparing to unpack .../libappindicator3-1_0.4.92-3.1_armhf.deb ...
Unpacking libappindicator3-1 (0.4.92-3.1) ...
Selecting previously unselected package gir1.2-appindicator3-0.1.
Preparing to unpack .../gir1.2-appindicator3-0.1_0.4.92-3.1_armhf.deb ...
Unpacking gir1.2-appindicator3-0.1 (0.4.92-3.1) ...
Selecting previously unselected package gir1.2-gconf-2.0.
Preparing to unpack .../gir1.2-gconf-2.0_3.2.6-3_armhf.deb ...
Unpacking gir1.2-gconf-2.0 (3.2.6-3) ...
Selecting previously unselected package blueman.
Preparing to unpack .../blueman_1.99~alpha1-1+deb8u1_armhf.deb ...
Unpacking blueman (1.99~alpha1-1+deb8u1) ...
Selecting previously unselected package bluetooth.
Preparing to unpack .../bluetooth_5.23-2+rpi2_all.deb ...
Unpacking bluetooth (5.23-2+rpi2) ...
Selecting previously unselected package libjbig2dec0.
Preparing to unpack .../libjbig2dec0_0.11+20120125-1_armhf.deb ...
Unpacking libjbig2dec0 (0.11+20120125-1) ...
Selecting previously unselected package libgs9-common.
Preparing to unpack .../libgs9-common_9.06~dfsg-2+deb8u1_all.deb ...
Unpacking libgs9-common (9.06~dfsg-2+deb8u1) ...
Selecting previously unselected package libgs9.
Preparing to unpack .../libgs9_9.06~dfsg-2+deb8u1_armhf.deb ...
Unpacking libgs9 (9.06~dfsg-2+deb8u1) ...
Selecting previously unselected package ghostscript.
Preparing to unpack .../ghostscript_9.06~dfsg-2+deb8u1_armhf.deb ...
Unpacking ghostscript (9.06~dfsg-2+deb8u1) ...
Selecting previously unselected package indicator-application.
Preparing to unpack .../indicator-application_0.5.0-1_armhf.deb ...
Unpacking indicator-application (0.5.0-1) ...
Selecting previously unselected package libpaper-utils.
Preparing to unpack .../libpaper-utils_1.1.24+nmu4_armhf.deb ...
Unpacking libpaper-utils (1.1.24+nmu4) ...
Processing triggers for fontconfig (2.11.0-6.3) ...
Processing triggers for man-db (2.7.0.2-5) ...
Processing triggers for gnome-menus (3.13.3-6) ...
Processing triggers for desktop-file-utils (0.22-1) ...
Processing triggers for mime-support (3.58) ...
Processing triggers for dbus (1.8.20-0+deb8u1) ...
Processing triggers for hicolor-icon-theme (0.13-1) ...
Setting up fonts-droid (1:4.4.4r2-6+rpi1) ...
Setting up imagemagick-common (8:6.8.9.9-5+deb8u3) ...
Setting up libdbusmenu-glib4:armhf (12.10.2-1) ...
Setting up libdbusmenu-gtk3-4:armhf (12.10.2-1) ...
Setting up libijs-0.35:armhf (0.35-10) ...
Setting up liblqr-1-0:armhf (0.4.2-2) ...
Setting up libmagickcore-6.q16-2:armhf (8:6.8.9.9-5+deb8u3) ...
Setting up libmagickwand-6.q16-2:armhf (8:6.8.9.9-5+deb8u3) ...
Setting up libpaper1:armhf (1.1.24+nmu4) ...

Creating config file /etc/papersize with new version
Setting up libpulse-mainloop-glib0:armhf (5.0-13) ...
Setting up libopenobex1 (1.5-2.1) ...
Setting up obex-data-server (0.4.5-1+b3) ...
Setting up notification-daemon (0.7.6-2) ...
Setting up gir1.2-notify-0.7 (0.7.6-2) ...
Setting up python-gi-cairo (3.14.0-1) ...
Setting up libindicator3-7 (0.5.0-2) ...
Setting up libappindicator3-1 (0.4.92-3.1) ...
Setting up gir1.2-appindicator3-0.1 (0.4.92-3.1) ...
Setting up gir1.2-gconf-2.0 (3.2.6-3) ...
Setting up blueman (1.99~alpha1-1+deb8u1) ...
Setting up bluetooth (5.23-2+rpi2) ...
Setting up libjbig2dec0 (0.11+20120125-1) ...
Setting up libgs9-common (9.06~dfsg-2+deb8u1) ...
Setting up libgs9 (9.06~dfsg-2+deb8u1) ...
Setting up ghostscript (9.06~dfsg-2+deb8u1) ...
Setting up indicator-application (0.5.0-1) ...
Setting up libpaper-utils (1.1.24+nmu4) ...
Processing triggers for libc-bin (2.19-18+deb8u4) ...
Processing triggers for dbus (1.8.20-0+deb8u1) ...
</pre>