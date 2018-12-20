# Kali-linux light with a Little Privacy !

Vagrant box with from kali-light (debian) on VirtuaBox

## What it includes

* Base image from [offensive-security/kali-linux-light](https://app.vagrantup.com/offensive-security/boxes/kali-linux-light)
* Language set to en_US.UTF-8
* net-tools (mostly for ifconfig command)
* git
* Tilix (better terminal)
* [4nonimizer](https://github.com/Hackplayers/4nonimizer)
* [Nipe](https://github.com/GouveaHeitor/nipe)

## Installation

1. `$ git clone git@github.com:nicmilot/kali-light-lp.git`
2. `$ cd kali-light-lp/vm`
3. `$ vagrant up`

### To do after first boot

1. Login and open tilix
2. Setup and enable 4nonimizer
    * `$ cd Desktop/4nonimizer`
    * `$ sudo su`
3. Go get [credentials](https://www.vpnbook.com/#openvpn) and install (for more privacy, see Nipe below)
    * `$ chmod +x 4nonimizer`
    * `$ ./4nonimizer install`
    * `$ ./4nonimizer start`
4. Look if it works
    * `$ ./4nonimizer vpn_status`
5. Continue setup
    * `$ ./4nonimizer enable_dns`
    * `$ ./4nonimizer vpn_status`

### Install Nipe
Nipe is a script to make the Tor network your default gateway.

* `$ cd Desktop/nipe`
* `$ sudo su`
* `$ cpan install Switch JSON LWP::UserAgent`
* `$ perl nipe.pl install`
* `$ apt-get update && apt-get update --fix-missing`
* `$ apt-get upgrade -y && apt-get dist-upgrade -y`
* `$ perl nipe.pl install`
* `$ perl nipe.pl start`
* `$ perl nipe.pl status`