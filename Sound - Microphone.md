###First -> Plug the USB microphone in and then reboot the RPi3!

[Good walk through of alsamixer (YouTube)](http://asliceofraspberrypi.blogspot.com/2013/02/adding-audio-input-device.html)

- Use alsamixer to set microphone record level  

<pre>
$ <b>arecord -l</b>

**** List of CAPTURE Hardware Devices ****
card 1: Device [USB PnP Sound Device], device 0: USB Audio [USB Audio]
  Subdevices: 1/1
  Subdevice #0: subdevice #0
</pre>


- To record

<pre>
$ <b>arecord -D plughw:1,0</b> <em>test.wav</em>

</pre>

- To play

<pre>
$ <b>omxplayer</b> <em>test.wav</em>  

$ <b>aplay</b> <em>test.wav</em>
</pre>
