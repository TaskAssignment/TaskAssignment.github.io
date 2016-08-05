---
layout: default
---

# [General Extractor]

This python3 script crawls the BugZilla platforms to read
and extract all the information related to the bugs that
are reported on these platforms

 - Mozilla
 - Eclipse
 - Kernel
 - LibreOffice

 To add more projects please add the urls and the
 XPATH directions (some of them are specified)
 to learn more about integrating more platforms to the
 system please check the TaskAssignment documentation


## Installation

This script is written in python3 hence it needs
to install the python dependencies by running

 - `$ pip3 install -r requirements.txt`

That text file is included in the same folder

If you get an error including any dependencies try:

 - `$ sudo apt-get install python-dev libxml2-dev libxslt1-dev zlib1g-dev`

## How to use

The commands to run this script are

Show services available:

 - `$ python3 generalextractor.py mean-prod showservices`

Show projects from a service:

 - `$ python3 generalextractor.py mean-prod showprojects mozilla`

Extract bugs from a specific project inside a service (Might take up to 1 hour):

 - `$ python3 generalextractor.py mean-prod mozilla aus`

## Examples


- `$ python3 generalextractor.py mean-prod showprojects bugzilla`
- `$ python3 generalextractor.py mean-prod showservices`
- `$ python3 generalextractor.py mean-prod mozilla toolkit`


## Troubleshooting

- If the project of the service you want to extract contains
spaces, replace them using "%20" to run it in console.

- The description and documentation of each method
is in the source code of the generator.

- You might want to generate the documentation website
out of this by using pydocs.

- If any user in the db contains "nobody" instead of
the real names it's because the information was not complete

- The first parameter "mean-prod" is the name of the database
where you want to save the information

- In the method "getBugs()" you can disable the fourth line
if you only want to retrieve the bugs with resolution=---

- The source code includes comments on every method 

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
