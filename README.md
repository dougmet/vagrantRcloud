# Installing RCloud onto a Vagrant Box

This is a recipe for installing [RCloud](https://github.com/att/rcloud) onto a [Vagrant](http://www.vagrantup.com) box running Ubuntu 14.04 Trusty.

The last version I tried is RCloud v1.4 on R 3.2.

Clone the directory where you like. Edit the rcloud.conf file to include your own GitHub app client ID and secret. Then hit

```
> vagrant up
```

From your favourite terminal. This will take ages.

Once you've successfully installed RCloud for the first time you can edit the allocated RAM in the VagrantFile from 4096MB to whatever you like. When compiling the Guitar package I've found you need a lot of RAM.

To use it back on your host browse to http://192.168.33.10:8080/login.R, authenticate on GitHub and you're off. Probably.

### GitHub App

For authentication you need to setup your own GitHub developer application https://github.com/settings/developers. You copy the client ID and secret into the correponding parts of the rcloud.conf file. My developer app looks like this:

![An example of a GitHub developer application](https://raw.github.com/dougmet/vagrantRcloud/master/githubdev.png)


### Comments

- solr is disabled.
- Everything is run as root. In a future version might want to add a provisioning script without sudo rights.
- Some issues with github were fixed by [this](https://github.com/att/rcloud/issues/1497).
