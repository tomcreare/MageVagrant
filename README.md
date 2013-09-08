MageVagrant
===============

MageVagrant is a complete LAMP development environment for Magento, forked from https://github.com/ucommerzapps/MageVagrant 


## Requirements

You will need the following software installed:

- Vagrant (www.vagrantup.com)
- Virtual Box (https://www.virtualbox.org/)


## Installation 

Getting MageVagrant up and running is as easy cloning the repo 

````git clone https://github.com/tomcreare/MageVagrant.git dev_box````

And running the Vagrant box

````
cd dev_box/
vagrant up
````

To connect:

````
vagrant ssh
````


This will setup a full LAMP development environment

You'll need to know how to setup basic virtual hosts in apache and edit your /etc/hosts to point to your wanted domain