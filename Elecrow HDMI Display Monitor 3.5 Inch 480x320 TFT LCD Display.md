Amazon:  
https://smile.amazon.com/gp/product/B013JEV6VA/ref=oh_aui_detailpage_o02_s00?ie=UTF8&psc=1#Ask

Company:   
http://www.elecrow.com/35-inch-480x320-tft-display-with-touch-screen-for-raspberry-pi-p-1385.html

1) Download .tarz for the .img file (1.7GB takes long time)  
2) Decompress .tarz (takes time)  
3) Check mounted disks "<b>df -h</b>"
<pre>
Filesystem      Size   Used  Avail Capacity iused      ifree %iused  Mounted on
/dev/disk1     465Gi   70Gi  394Gi    16% 1640055 4293327224    0%   /
devfs          183Ki  183Ki    0Bi   100%     634          0  100%   /dev
map -hosts       0Bi    0Bi    0Bi   100%       0          0  100%   /net
map auto_home    0Bi    0Bi    0Bi   100%       0          0  100%   /home
</pre>
3) Put SD card in and check again "<b>df -h</b>"
<pre>
Filesystem      Size   Used  Avail Capacity iused      ifree %iused  Mounted on
/dev/disk1     465Gi   80Gi  385Gi    18% 1640215 4293327064    0%   /
devfs          189Ki  189Ki    0Bi   100%     654          0  100%   /dev
map -hosts       0Bi    0Bi    0Bi   100%       0          0  100%   /net
map auto_home    0Bi    0Bi    0Bi   100%       0          0  100%   /home
<b>/dev/disk2s6</b>    66Mi   21Mi   45Mi    32%     512          0  100%   /Volumes/boot
<b>/dev/disk2s1</b>   2.3Gi  2.2Gi   90Mi    97%       0          0  100%   /Volumes/RECOVERY
</pre>
4) Unmount <b>BOTH</b> SD card disks so nothing interfers with the write
$ <b>sudo diskutil umount /dev/disk2s6</b>
<pre>
Volume boot on disk2s6 unmounted
</pre>
$ <b>sudo diskutil umount /dev/disk2s1</b>
<pre>
Volume RECOVERY on disk2s1 unmounted
</pre>
5) Write .img to SD card (does not show update status, takes a long time)
$ <b>sudo dd bs=4m if=RPi-35inch-LCD-Raspbian-160728.img of=/dev/disk2</b>
<pre>
1847+0 records in
1847+0 records out
7746879488 bytes transferred in 3583.259509 secs (2161964 bytes/sec)
</pre>
6) Plug 3.5 monitor in and reboot  
9) <b>sudo apt-get update</b>
