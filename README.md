# ezMage Legacy

A basic preprovisioned dev box for Magento 1 development

- Debian Stretch
- Apache
- redis
- MariaDB
- PHP 5.6
- composer
- Xdebug
- MailCatcher
- phpMyAdmin

## Start up ezMage Legacy
Assuming that VirtualBox (https://www.virtualbox.org/) and Vagrant (https://www.vagrantup.com/) are already installed on your machine...

1. Clone or download + unzip repository
2. In your terminal go to the directory and type `vagrant up`
3. Enjoy

## Using ezMage Legacy


The default configuration of the box uses the ip 192.168.33.77.


You should make an entry in your /etc/hosts file for the domain. E.g

`192.168.33.77 magento-dev.local`


#### MailCatcher
Any emails your application sends are caught by MailCatcher, which can be accessed from:
http://192.168.33.77:1080

#### MySQL
Connection details for the MySQL database are:

**database:** magento
**user:** root
**password:** 123

phpMyAdmin can be accessed from http://192.168.33.77/phpmyadmin

## Magento setup

Log in to the vagrant

```
vagrant ssh

```

#### IP Address
You can change the ip of the box by editing the following line in the `Vagrantfile` and replacing 192.168.33.77 with the ip you'd like to use:

`config.vm.network "private_network", ip: "192.168.33.77"`
