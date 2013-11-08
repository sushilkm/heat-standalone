heat-standalone
==========================

Install script to get standalone heat server on ubuntu running against devstack and 
some simple heat templates that will work with it.

Tested with ubuntu 12.04

Configuration
--------------
You probably want to create a localrc file and set all or some of these
configuration variables. It will be sourced by the install-heat shell script.

 - DATABASE_PASSWORD
 - RABBITMQ_PASSWORD
 - REGION (ex. RegionOne)
 - AUTH_SERVER (IP of server where devsatck is running)
 - HEAT_ADMIN_PASSWORD (Password for heat admin account, admin account used is "heat" and admin tenant is "service")

If no localrc file exists, default values will be used. They are defined
at the top of the install-heat script.

Installation Steps
----------------------------

$ sudo apt-get update

$ sudo apt-get install git-core -y

$ git clone https://github.com/sushilkm/heat-standalone

$ cd heat-standalone

$ ./install-heat

Enter the requested parameters.


After Installation finishes, start the api and engine services, using:

sudo heat-api &

sudo heat-engine &

