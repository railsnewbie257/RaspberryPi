###Change the Timezone

$ <b>sudo dpkg-reconfigure locales</b>
<pre>
Scroll down to the option you want and use the space bar to select/unselect

<em>unselect</em> en_GB.UTF-8 UTF-8
<em>select</em>   en_US.UTF-8 UTF-8

<em>tab</em>
<em>select</em> OK
</pre>

$ <b>sudo dpkg-reconfigure keyboard-configuration</b>  

$ <b>sudo dpkg-reconfigure tzdata</b>
