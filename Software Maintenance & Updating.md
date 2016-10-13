###[Updating Raspbian](https://www.youtube.com/watch?v=-6OGuhLtKbU&t=15m52s)

<em>to update trees</em>   
$ <b>sudo apt-get update</b>   

    An update must be performed first so that apt-get knows that 
    new versions of packages are available.
    
<em>Check which to use between **update** and **dist-update**</em>  

$ <b>sudo apt-get upgrade</b>   

    upgrade is used to install the newest versions of all packages
    currently installed on the system from the sources enumerated in
    /etc/apt/sources.list. Packages currently installed with new
    versions available are retrieved and upgraded; under no
    circumstances are currently installed packages removed, or packages
    not already installed retrieved and installed. New versions of
    currently installed packages that cannot be upgraded without
    changing the install status of another package will be left at
    their current version. 

$ <b>sudo apt-get dist-upgrade</b> 

    dist-upgrade in addition to performing the function of upgrade,
    also intelligently handles changing dependencies with new versions
    of packages; apt-get has a "smart" conflict resolution system, and
    it will attempt to upgrade the most important packages at the
    expense of less important ones if necessary. So, dist-upgrade
    command may remove some packages. The /etc/apt/sources.list file
    contains a list of locations from which to retrieve desired package
    files. See also apt_preferences(5) for a mechanism for overriding
    the general settings for individual packages.
    
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
