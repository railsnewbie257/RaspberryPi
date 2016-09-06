###Pinout
USB Microphone -> RPi3 USB  
USB Keyboard -> RPI3 USB  (need this for resetting up)  
HDMI Cable RPi3 -> TV


###Alexa Voice Service - Videos to watch:

###1. Original [Sam Machin article](http://sammachin.com/the-10-echo/)  
link to **ORIGINAL** github repository which gets updated

<pre>
git clone https://github.com/sammachin/AlexaPi.git   
</pre>

Novospirit Tech Github Repository (frozen copy goes with this [video](https://www.youtube.com/watch?v=frH9HaQTFL8)): 

<pre>
git clone https://github.com/novaspirit/AlexaPi.git
</pre>

###2. [Installing Alexa Voice Service to Raspberry Pi (YouTube)](https://www.youtube.com/watch?v=frH9HaQTFL8)
(showed how to setup the URLs in Amazon Development for access)

###3. [How to Build an Amazon Echo Raspberry Pi | From Start To Finish (YouTube)](https://www.youtube.com/watch?v=d2KvT8tcmNU)  
(seems to be a copy of #2, but does show how to hack a button press)

explains entire setup on Raspberry Pi  
<pre>
Uses GPIO #18

<a href=https://www.youtube.com/watch?v=d2KvT8tcmNU&t=21m27s>Simulate button press without button - pull GPIO #18 to GND while asking question</a>
</pre>

###Instructions

1. Download Git repository

<pre>
git clone https://github.com/sammachin/AlexaPi.git   
</pre>

This will create the directory `AlexaPi`.  

<pre>
<b>cd AlexaPi</b>
<b>sudo ./setup.sh</b>

<em>you will need Amazon developer credentials to fill in some questions</em>
</pre>

2. Create developer account at http://developer.amazon.com   

Using as railsnewbie257@gmail.com
<pre>
To find an already registered device go to Developer Console:  
- Alexa Voice Services  
- Edit  
- page through to get security codes and things
</pre>

3. After filling in Amazon Development credentials

###[Setup on Raspberry Pi (YouTube)](https://www.youtube.com/watch?v=d2KvT8tcmNU&t=17m53s0)
<pre>
CherryPy Checker:
The Application mounted at '' has an empty config.

[04/Sep/2016:02:17:15] ENGINE Started monitor thread 'Autoreloader'.
[04/Sep/2016:02:17:15] ENGINE Started monitor thread '_TimeoutMonitor'.
[04/Sep/2016:02:17:15] ENGINE Serving on http://0.0.0.0:5000
[04/Sep/2016:02:17:15] ENGINE Bus STARTED
</pre>

in a web browser goto <em>raspberry-ip-address</em> (could be 192.168.1.101:5000 same as in Amazon Developer)  
You will see the authorization ticket  
Then Ctrl-C

<pre>
^C[04/Sep/2016:02:18:02] ENGINE Keyboard Interrupt: shutting down bus
[04/Sep/2016:02:18:02] ENGINE Bus STOPPING
[04/Sep/2016:02:18:02] ENGINE HTTP Server cherrypy._cpwsgi_server.CPWSGIServer(('0.0.0.0', 5000)) shut down
[04/Sep/2016:02:18:02] ENGINE Stopped thread '_TimeoutMonitor'.
[04/Sep/2016:02:18:02] ENGINE Stopped thread 'Autoreloader'.
[04/Sep/2016:02:18:02] ENGINE Bus STOPPED
[04/Sep/2016:02:18:02] ENGINE Bus EXITING
[04/Sep/2016:02:18:02] ENGINE Bus EXITED
[04/Sep/2016:02:18:02] ENGINE Waiting for child threads to terminate...
Open http://192.168.1.101 :5000
You can now reboot
</pre>

then

<pre>
<b>sudo shutdown -r now</b>
</pre>


<pre>
<b>sudo ./setup.sh</b>
</pre>

###[ifttt - if then that](https://ifttt.com)

###Robot

[Mars Curiosity inspired Rover (blog)](http://letsmakerobots.com/node/49149)
