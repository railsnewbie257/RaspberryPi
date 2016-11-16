###Making new SSH Keys

$ <b>ssh pi@</b><em>192.168.1.7</em>
<pre>
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@    WARNING: REMOTE HOST IDENTIFICATION HAS CHANGED!     @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
IT IS POSSIBLE THAT SOMEONE IS DOING SOMETHING NASTY!
Someone could be eavesdropping on you right now (man-in-the-middle attack)!
It is also possible that a host key has just been changed.
The fingerprint for the ECDSA key sent by the remote host is
SHA256:DCFcWMNtHbME6CjRIsCvDeVNs5lsxwF44Plh/bHzYCI.
Please contact your system administrator.
Add correct host key in /Users/peterpih/.ssh/known_hosts to get rid of this message.
Offending ECDSA key in /Users/peterpih/.ssh/known_hosts:19
ECDSA host key for 192.168.1.7 has changed and you have requested strict checking.
Host key verification failed.
</pre>

###On the RPi
$ <b>cd /etc/ssh</b>   
$ <b>del ssh_host_*</b>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# <em>delete the existing keys</em>   
$ <b>ssh-keygen -A</b>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;#<em> generates all the keys</em>   
<pre>
Will produce message saying keys are being generated
</pre>

###On host side
1) <em>edit</em> <b>~/.ssh/known_hosts</b>   
2) find the line with the ip address, delete the line, and save the file   

$ <b>ssh pi@</b><em>192.168.1.7</em>
<pre>
The authenticity of host '192.168.1.7 (192.168.1.7)' can't be established.
ECDSA key fingerprint is SHA256:Xln98vM7ztd2rDdkZAuqy52+Kio2g6aOaELDWQnWa9I.
Are you sure you want to continue connecting (yes/no)? y
Please type 'yes' or 'no': yes
Warning: Permanently added '192.168.1.7' (ECDSA) to the list of known hosts.
pi@192.168.1.7's password: 

The programs included with the Debian GNU/Linux system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Debian GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
permitted by applicable law.
Last login: Thu Jul 28 18:29:09 2016
</pre>

You have now logged in with new ssh keys
