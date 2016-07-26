####For general updating
<pre>
sudo apt-get update   # <em>to update trees</em>
sudo apt-get upgrade  # <em>to actually update</em>
sudo apt_get clean   #<em> to clean up</em>
</pre>

####To update Node.js (also see [here](https://www.raspberrypi.org/forums/viewtopic.php?f=34&t=140747))
<pre>
sudo apt-get remove node* npm*
...
# <em>will auto update</em>
...
sudo apt_get autoremove   # <em>to clean up</em>
</pre>
