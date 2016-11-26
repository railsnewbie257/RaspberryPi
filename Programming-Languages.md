###[Installing Elixir (elixir.org)](http://elixir-lang.org/install.html)

###[Elixir on the Raspberry Pi - Blinking an LED](https://wtfleming.github.io/2015/12/10/embedded-elixir-raspberry-pi/)

<pre>
*********************************************************************
**********************  APPLICATIONS INFORMATION  *******************
*********************************************************************

wx             : wxWidgets not found, wx will NOT be usable

*********************************************************************
*********************************************************************
**********************  DOCUMENTATION INFORMATION  ******************
*********************************************************************

documentation  : 
                 xsltproc is missing.
                 fop is missing.
                 xmllint is missing.

                The documentation can not be built.

*********************************************************************
</pre>

$ <b>sudo apt-get install xsltproc</b>   
$ <b>sudo apt-get install fop</b>    
$ <b>sudo apt-get install libxml2-dev</b>


$ <b>./configure --without-wx</b>    
If you need **wx** support, see [instructions](http://www.erlang.org/doc/installation_guide/INSTALL.html) at **Building with wxErlang** section.
 
