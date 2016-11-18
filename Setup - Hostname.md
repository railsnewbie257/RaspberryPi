$ <b>hostname</b>
<pre>
raspberrypi
</pre>


###Changing the hostname

1) edit <b>/etc/hosts</b>
<pre>
127.0.0.1	     localhost
::1		         localhost ip6-localhost ip6-loopback
ff02::1		     ip6-allnodes
ff02::2		     ip6-allrouters

127.0.1.1	     <b>RPi-35display</b>
</pre>

2) edit <b>/etc/hostname</b>
<pre>
<b>RPi-35display</b>
</pre>

3) commit changes  
$ <b>sudo /etc/init.d/hostname.sh</b>  

4) reboot  
$ <b>sudo reboot</b>

$ <b>hostname</b>
<pre>
RPi-35display
</pre>

####Add Bonjour so can discover RPi using hostname not ip addr
$ <b>sudo apt-get update</b>  
$ <b>sudo apt-get install libnss-mdns</b>  

The from laptop
$ <b>ping -c 4</b> <em>RPi-35display</em><b>.local</b>
