####[Setup email on Raspberry Pi](http://www.sbprojects.com/projects/raspberrypi/exim4.php)

####Modify the config file

<b>sudo nano /etc/ssmtp/ssmtp.conf</b>   # <em>edit config file</em>
<pre>
# <em>change mailhub to use gmail</em>
<b>mailhub=smtp.gmail.com:587</b>

# <em>these lines may need to be added or changed</em>
<b>AuthUser=</b><em>use-address</em><b>@gmail.com</b>
<b>AuthPass=</b><em>email-password</em>
<b>useSTARTTLS=Yes</b>

</pre>

####Sending email
<pre>
<b>mail -s</b> <em>"This is the subject line" send-address@email.com</em>
<b>cc:</b> <em>return if none</em>
...
<em>body of email here</em>
...
</pre>

end with ^D
