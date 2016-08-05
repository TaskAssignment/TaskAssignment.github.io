---
layout: default
---

# [deploymentTools]

To deploy the project I have created a Vagrant box to ensure portability
and ease of development, this makes easy to install the environment on
every computer regarding the OS. It uses Vagrant

The current software installed in the box are

- mongodb
- git
- nodejs
- npm install
- python3
- pip3

This Vagrant box can be easily deployed to any
Openstack or virtual machine hosting service by

## Installation

Please install Vagrant first

From this [https://www.vagrantup.com/downloads.html](https://www.vagrantup.com/downloads.html)

and make sure that you can run vagrant in your system without problems

## How to use

Download the Vagrant box at Google Drive

[https://drive.google.com/open?id=0B1ymt5yabalHdnlkci1xNWRzb3M](https://drive.google.com/open?id=0B1ymt5yabalHdnlkci1xNWRzb3M)

Run the environment with

 - `$ vagrant box add software_expertise software_expertise.box`
 - `$ vagrant init software_expertise`
 - `$ vagrant up`
 - `$ vagrant ssh`

 This will start the VM (virtual machine)
 and you'll be able to use it

## Important

These commands are used every day to start and
log in to the VM

**This command might take a while the first time**

 - `$ vagrant up`

Login to the virtual machine:

 - `$ vagrant ssh`


## Installed software


- MongoDB v3.2.8

- Git v2.7.4

- Node.js v6.3.1

- NPM v3.10.3

- Python v3.5.2

- PIP3 v8.1.1

## Command use for the configuration of the Vagrant Box


This Vagrant box was built using Ubuntu 16.04
on top of [https://atlas.hashicorp.com/bento/boxes/ubuntu-16.04](https://atlas.hashicorp.com/bento/boxes/ubuntu-16.04)


Install important general dependencies

- `$ sudo apt-get update`
- `$ sudo apt-get upgrade`
- `$ sudo apt-get install build-essential libssl-dev libcurl4-gnutls-dev libexpat1-dev gettext unzip`

Install git

- `$ sudo apt-get install git`

Install mongodb

- `$ sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv EA312927`
- `$ echo "deb http://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/3.2 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.2.list`
- `$ sudo apt-get install -y mongodb-org`

Install node.js and required libraries

The libraries

- `$ sudo apt install curl`
- `$ apt-get install make g++ libssl-dev git`
- `$ sudo apt-get update`

The package

- `$ cd /tmp`
- `$ wget https://nodejs.org/dist/v6.3.1/node-v6.3.1.tar.gz`
- `$ tar -xvf node-v6.3.1.tar.gz`
- `$ cd node-v6.3.1`
- `$ ./configure`
- `$ make -j2`
- `$ make install`


Install pip3

`$ sudo apt-get -y install python3-pip`

The following is to make sure the python3 dependencies will run

`$ sudo apt-get install python-dev libxml2-dev libxslt1-dev zlib1g-dev`


## Author & Support

* [Diego Zamora Rodriguez](zamoraro@ualberta.ca)
