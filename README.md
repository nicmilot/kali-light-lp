# Kali-linux light with a Little Privacy !

## What it includes

* Base image from [offensive-security/kali-linux-light](https://app.vagrantup.com/offensive-security/boxes/kali-linux-light)
* Language set to en_US.UTF-8
* net-tools (mostly for ifconfig command)
* git
* [4nonimizer](https://github.com/Hackplayers/4nonimizer)

## Installation

1. `touch Vagrantfile`
2. `nano Vagrantfile`

    ```Vagrantfile
    Vagrant.configure("2") do |config|
        config.vm.box = "nicmilot/kali-light-lp"
        config.vm.box_version = "1.0.0"
    end
    ```

3. Vagrant up

### To do after first boot

1. Login and open terminal
2. Setup and enable 4nonimizer
    * `$ cd Desktop/4nonimizer`
    * `$ sudo su`
3. Go get [credentials](https://www.vpnbook.com/#openvpn) and install
    * `$ sudo chmod +x 4nonimizer`
    * `$ ./4nonimizer install`
    * `$ ./4nonimizer start`
4. Look if it works
    * `$ ./4nonimizer vpn_status`
5. Continue setup
    * `$ ./4nonimizer proxychains4`
    * `$ ./4nonimizer enable_dns`
    * `$ ./4nonimizer browser`
    * `$ ./4nonimizer status`