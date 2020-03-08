# Ansible OpenWrt Builder

This is a simple playbook for setting up a compiling environment for OpenWrt.


## Requirements

You should provide a VM or server where you have root privileges.

This playbook is compatible with Debian 10. 

It will install all required packages, clone openwrt repository and execute the initial install scripts.


## Usage

Specify the host ip on `hosts.ini`, then execute `ansible-playbook -i hosts.ini openwrt-compiler.yml -u root`.




Next you can login as user **forger**, go to */home/forger/openwrt/* and execute `make menuconfig` to launch the config interface. Choose your desired settings and execute `make` to start compilation.

These steps are based on OpenWrt [Image Building Guide](https://openwrt.org/docs/guide-developer/quickstart-build-images).
