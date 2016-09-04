- Plug headphones in
- find file "example.mp3"

- if you do not have an exmaple.mp3 file, download one at:   

<pre>
$ <b>wget https://goo.gl/XJuOUW -O example.mp3 --no-check-certificate</b>  

 --2016-09-03 14:50:09--  https://goo.gl/XJuOUW
Resolving goo.gl (goo.gl)... 172.217.4.142, 2607:f8b0:4007:808::200e
Connecting to goo.gl (goo.gl)|172.217.4.142|:443... connected.
HTTP request sent, awaiting response... 301 Moved Permanently
Location: https://raw.githubusercontent.com/raspberrypilearning/burping-jelly-baby/master/sounds/la.mp3 [following]
--2016-09-03 14:50:10--  https://raw.githubusercontent.com/raspberrypilearning/burping-jelly-baby/master/sounds/la.mp3
Resolving raw.githubusercontent.com (raw.githubusercontent.com)... 151.101.48.133
Connecting to raw.githubusercontent.com (raw.githubusercontent.com)|151.101.48.133|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 17260 (17K) [audio/mpeg]
Saving to: ‘example.mp3’


example.mp3                   100%[===================================================>]  16.86K  --.-KB/s   in 0.03s  

2016-09-03 14:50:10 (667 KB/s) - ‘example.mp3’ saved [17260/17260]
</pre>

- Then to play use
<pre>
$ <b>omxplayer</b> <em>example.mp3</em>
</pre>

aplay not working but omxplayer is   
https://www.raspberrypi.org/forums/viewtopic.php?f=91&t=7663   
https://gist.github.com/mcandre/b11c0817d0f3976a9840   
