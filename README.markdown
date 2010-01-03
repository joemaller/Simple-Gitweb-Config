##gitweb_config.perl

This is an example configuration file for simple, non-compiled deployments
of Gitweb.

Authored by Joe Maller on January 2, 2010   
Based on Git source version 1.6.6   
<http://github.com/joemaller/Simple-Gitweb-Config>


###Instructions for installing Gitweb without building or compiling

1. On your webserver, download and extract current Git source
2. Inside gitweb directory, rename **gitweb.perl** -> **gitweb.cgi**
3. In **gitweb.cgi**, line 546, inserting the name of this file:   
	`-our $GITWEB_CONFIG = $ENV{'GITWEB_CONFIG'} || "++GITWEB_CONFIG++";`   
	`+our $GITWEB_CONFIG = $ENV{'GITWEB_CONFIG'} || "gitweb_config.perl";`
4. Copy the Simple Gitweb Config files into your gitweb.cgi directory
5. Edit **gitweb\_config.perl**, **projects\_list.txt** and the three optional html 
   files for your local configuration 


### The gitweb_config.perl file is broken up into two sections:

1. Local Configuration   
Gitweb won't work at all without these.

2. Rarely Used   
If you're customizing these settings, this probably isn't for you.
