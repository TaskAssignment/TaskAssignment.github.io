---
layout: default
---

# [deploymentTools]

To deploy the project I have created a Vagrant box to ensure portability
and ease of development

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

From this [link](https://www.vagrantup.com/downloads.html)

and make sure that you can run vagrant in your system without problems

## How to use

The commands to run this script are

Set the VagrantFile:

 - `$ vagrant init mybox.box`

Starts the virtual machine:

**This make take a lot of time the first time, make sure
you have an Internet connection**

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


Install important general dependencies

- `$ sudo apt-get update
- `$ sudo apt-get upgrade
- `$ sudo apt-get install build-essential libssl-dev libcurl4-gnutls-dev libexpat1-dev gettext unzip

Install git

- `$ sudo apt-get install git

Install mongodb

- `$ sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv EA312927
- `$ echo "deb http://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/3.2 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.2.list
- `$ sudo apt-get install -y mongodb-org

Install node.js and required libraries

- `$ sudo apt install curl
- `$ apt-get install make g++ libssl-dev git
- `$ sudo apt-get update

`$ cd /tmp
$ wget https://nodejs.org/dist/v6.3.1/node-v6.3.1.tar.gz
$ tar -xvf node-v6.3.1.tar.gz
$ cd node-v6.3.1
$ ./configure
$ make -j2
$ make install
`

Install pip3

`$ sudo apt-get -y install python3-pip`



## How to add more services

If you want to add more services

1. Add the necesary URLS to the dictionaries related.

    - login
    - base
    - components
    - bugs
    - history
    - prefix

2. Make sure the new platform has a user registered as the rest. You can register
  new users for all the platforms but all of them must have the same one.

3. Add the XPath to the data (ids, components and projects). For most
  of them are handled but in case is diferent just add "|" and the path.

4. Run the script with the new platform, make sure the name of the new
  service doesn't conflict with the rest.

Remember that depending on the provider the field names and other things might change

## Documentation

You can check the source code for the detailed description of each method

## Author & Support

* [Diego Zamora Rodriguez](zamoraro@ualberta.ca)
