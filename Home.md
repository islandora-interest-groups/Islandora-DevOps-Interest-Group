# Islandora DevOps Special Interest Group

## What is an Islandora Server?

### Development Box (All Roles or Services on one standalone VM or PC) 
* Database Server - MySQL
* Repository Server - Fedora Commons
* Web Server - Apache	

### Production Server(s) (Individual Servers/VMs for each Role)
* Database Server - MySQL
* Repository Server - Fedora Commons
* Web Server - Apache

## What are the system requirements of Islandora?
	
### Development Box (All Roles or Services on one standalone VM or PC) 
#### Virtual Machine settings
##### Vagrant [https://www.vagrantup.com/](https://www.vagrantup.com/)
##### Virtualbox (Windows, OSX, Linux) [https://www.virtualbox.org/](https://www.virtualbox.org/)
##### VMWare	
(OSX - Fusion) [http://www.vmware.com/products/fusion/](http://www.vmware.com/products/fusion/)  
(Windows - Workstation) [http://www.vmware.com/products/workstation/](http://www.vmware.com/products/workstation/)
#### Minimal Requirements: (examples)
> 1 x 2.0 GHz Intel Core i3 CPU (x64)

> 2 GB RAM 1600 Mhz DDR3

> 10 GB Storage	
		
#### Recommended Settings: (examples)
> 1 x 2.6 GHz Intel Core i7 CPU (x64)

> 8 GB RAM 1600 Mhz DDR3

> 140 GB Storage

### Production Server(s) (Individual Servers for each Role)
#### Virtual Machine settings
##### Virtualbox
##### VMWare	

#### Minimal Requirements: (examples)
		
##### Recommended Settings by Server or Role:
###### Database Server - MySQL
###### Repository Server - Fedora Commons
###### Web Server - Apache
			
###### SELINUX configurations
###### IP Table configurations
###### List of Ports and Protocols

***A connectivity diagram would be ideal here especially how production servers connect to each other***

## What are the software/role requirements of Islandora? 
- Regardless of being a production or all-in-one
- Also broken down by operating system to highlight differences
- On RHEL/CENTOS, recommended to turn off iptables & SELINUX set to permissive 

See accompanying spreadsheet (Islandora DevOps Server Requirements) for results for:
- Debian / Ubuntu 14.04 (LTS)
- Red Hat Enterprise Linux / CENTOS 6.6

## I can’t find my use case or server, tool etc?
Submitted Case Studies will be reviewed in an ongoing basis, curated and entered into the tables above for “real world” best practices, additional operating systems, alternative relational databases or other technological outliers to further inform current users and/or potential adopters of Islandora.

## What configuration management tools can I use to deploy Islandora?
- Ansible
- Salt
- Chef
- Puppet