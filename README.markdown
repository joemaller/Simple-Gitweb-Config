##gitweb_config.perl

This is an example configuration file for simple, non-compiled deployments
of Gitweb.

Authored by Joe Maller, January 2010   
Based on Git v1.6.6   

**Download:** [zip](http://github.com/joemaller/Simple-Gitweb-Config/zipball/master) or [tar.gz](http://github.com/joemaller/Simple-Gitweb-Config/tarball/master)


###Instructions for installing Gitweb without building or compiling

1. On your webserver, download and extract the current Git source package, then copy the **gitweb** directory to your web root.
2. Inside the **gitweb** directory, rename **gitweb.perl** -> **gitweb.cgi**
3. Edit **gitweb.cgi** replacing `++GITWEB_CONFIG++` with `gitweb_config.perl` on line 546:   
     `-our $GITWEB_CONFIG = $ENV{'GITWEB_CONFIG'} || "++GITWEB_CONFIG++";`   
     `+our $GITWEB_CONFIG = `$ENV`{'GITWEB_CONFIG'} || "gitweb_config.perl";`
4. Download the **Simple Gitweb Config** files and extract them into the same directory as your **gitweb.cgi** files. At this point, Gitweb should be working.
5. If necessary, edit **projects\_list.txt**, **gitweb\_config.perl** and customize the three html files for your environment. 
