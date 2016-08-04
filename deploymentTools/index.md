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

## Installation


## How to use

The commands to run this script are

Show services available:

 - `$ python3 generalextractor.py showservices`

Show projects from a service:

 - `$ python3 generalextractor.py showprojects mozilla`

Extract bugs from a specific project inside a service (Might take up to 1 hour):

 - `$ python3 generalextractor.py mozilla aus`

## Examples


- `$ python3 generalextractor.py showprojects bugzilla`
- `$ python3 generalextractor.py showservices`
- `$ python3 generalextractor.py mozilla toolkit`


## Important



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
