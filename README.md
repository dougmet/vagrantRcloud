# Installing RCloud onto a Vagrant Box

This is a recipe for installing [RCloud](https://github.com/att/rcloud) onto a [Vagrant](http://www.vagrantup.com) box running Ubuntu 14.04 Trusty.

Clone the directory where you like. Edit the rcloud.conf file to include your own GitHub app client ID and secret. Then hit

```
> vagrant up
```

From your favourite terminal. This will take ages.

Once you've successfully installed RCloud for the first time you can edit the allocated RAM in the VagrantFile from 4096MB to whatever you like. When compiling the Guitar package I've found you need a lot of RAM.

To use it back on your host browse to http://192.168.33.10:8080/login.R, authenticate on GitHub and you're off. Probably.
