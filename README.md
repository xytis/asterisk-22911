asterisk-22911
==============

Virtual environment for exact bug replication.

Prerequisites:
- [virtualbox](https://www.virtualbox.org/wiki/Downloads)
- [vagrant](http://downloads.vagrantup.com/)
- [ansible](http://www.ansibleworks.com/docs/intro_installation.html)

Usage:

    vagrant up    # should download and start virtual machine then run ansible provision.
    
In case above fails -- try `vagrant provision` on booted vm, sometimes it is just stubborn.
