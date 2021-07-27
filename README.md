# Godb Setup

## Attempt with Ubuntu 18.04

Followed the guide from https://mac.getutm.app/gallery/ubuntu-20-04,
but *importantly* the 'Display' needs to be set to 'Console only' for
the 18.04 iso from:
http://old-releases.ubuntu.com/releases/bionic/ubuntu-18.04.4-server-arm64.iso

  * once ubuntu is installed the 'Display' can be reset to 'Full Graphics'
  * install a suitable desktop e.g. XFCE with

    sudo apt install tasksel
    sudo tasksel install xubuntu-desktop
    sudo reboot

*Package Installation*

    sudo apt-get install mongodb python-pymongo python-flask 
    sudo apt-get install tabix libhts2 libhts-dev
    sudo apt-get install python-pysam

*Packages not available via apt-get

  * flask_wtf
    * installed 0.14.3 due to a werkzueg dependency conflict with older versions
    * need to install from source via pip

    pip install -U https://github.com/wtforms/flask-wtf/archive/refs/tags/0.14.3.tar.gz




*Config of GoDb codebase*

This section will be obsolete as the codebase gets updated and is currently a 
working document.

    * all the config files in <root>/cfg need to be checked for valid paths
      * in particular 'common.cfg', 'godb.cfg' and 'webapp.cfg'
      * strikes me that they should be rationalised and be more agnostic



## Failed 20.04 Attempt

Followed this guide:

  https://medium.com/@lizrice/linux-vms-on-an-m1-based-mac-with-vscode-and-utm-d73e7cb06133
  https://mac.getutm.app/gallery/ubuntu-20-04

Start from Arm64 install of 20.04 Server

  https://cdimage.ubuntu.com/releases/20.04/release/ubuntu-20.04.2-live-server-arm64.iso

## Commands

After initial install of server

  1. Install Xubuntu GUI
    sudo apt install tasksel
    sudo tasksel install Xubuntu-desktop
    sudo reboot
  2. Intall software packages
    sudo apt-get install mongodb (v.3.6.8)
    sudo apt-get install python (v2.7.18)

*End* no python-flask is available for python2 on 20.04. Dead end.
