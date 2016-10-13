###[Updating Raspbian](https://www.youtube.com/watch?v=-6OGuhLtKbU&t=15m52s)

<em>to update trees</em>   
$ <b>sudo apt-get update</b>   

<em>upgrade all installed packages</em>  
$ <b>sudo apt-get dist-upgrade</b> 

<em>to actually update</em>  
$ <b>sudo apt-get upgrade</b>   

<em>to clean up afterwards</em>   
$ <b>sudo apt-get clean</b>   


###To update Node.js (also see [here](https://www.raspberrypi.org/forums/viewtopic.php?f=34&t=140747))

$ <b>sudo apt-get remove</b> <em>node* npm*</em>
<pre>
...
# <em>will auto update</em>
...
<b>sudo apt_get autoremove</b>   # <em>to clean up</em>
<b>curl -sL https://deb.nodesource.com/setup_6.x | sudo bash</b>   # <em>'6' is the version number</em>
<b>sudo apt-get install</b> <em>nodejs</em>  # <em>to install</em>
</pre>

$ <b>node -v</b>
<pre>
v6.3.1
</pre>
$ <b>npm -v</b>
<pre>
3.10.1
</pre>
