# Godb Setup

Followed this guide
https://medium.com/@lizrice/linux-vms-on-an-m1-based-mac-with-vscode-and-utm-d73e7cb06133
https://mac.getutm.app/gallery/ubuntu-20-04

Start from Arm64 install of 20.04 Server
https://cdimage.ubuntu.com/releases/20.04/release/ubuntu-20.04.2-live-server-arm64.iso

## Commands

After initial install of server

  1. Install Kubuntu GUI
    sudo apt install tasksel
    sudo tasksel install ubuntu-desktop
    sudo reboot
  2. Intall software packages
    sudo apt-get install mongodb (v.3.6.8)
    sudo apt-get install python (v2.7.18)
