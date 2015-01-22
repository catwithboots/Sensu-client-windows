sensu-client.net
================

An implementation of the sensu client in .NET for those that don't want to drag around a fully Ruby runtime on Windows. I'm not claiming this to be fully featured, but should support some task execution and simple checks.

Based on implementation from Growse

https://github.com/growse/sensu-client.net



Installation
============

The MSI will install a service called 'Sensu Client' and application into `%PROGRAMFILES%`. It provides a sample sensu-compatible json-based config file in the installation directory. Sensu-client.net will then log to `%PROGRAMDATA%\sensu-client.net\logs`.


Getting the ruby embedded
=========================

Download the embedded ruby from here:
[http://dl.bintray.com/oneclick/rubyinstaller/ruby-1.9.3-p551-i386-mingw32.7z?direct](http://dl.bintray.com/oneclick/rubyinstaller/ruby-1.9.3-p551-i386-mingw32.7z?direct "ruby 1.9.3-p551")
create a folder structure like: 
> C:\opt\sensu\embedded

and unzip the folder there (so you will eventually get this:

> C:\opt\sensu\embedded\bin <br>
> C:\opt\sensu\embedded\include<br>
> C:\opt\sensu\embedded\lib<br>
> C:\opt\sensu\embedded\share<br>

inside the \bin folder with a command prompt do a
> gem install sensu-plugin

then fork or download: [https://github.com/sensu/sensu-community-plugins](https://github.com/sensu/sensu-community-plugins)
(you can do a "Download ZIP" from the URL) and put the plugins in C:\opt\sensu\plugins.

Thats it for now...update needs to come for the included embedded ruby and correct plugin path.