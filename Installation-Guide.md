# Package Management

The approach to installing Docker largely depends on the package manager for LInux Distribution. APT (ubuntu/Debian) and YUM for (red-hat/Centos) are the two popular examples

# Launch EC2 Instance and connect through SSH Client
open command prompt
Connect to your EC2 instance using public DNS

Switch to root user : 		$ sudo -i

Rename Hostname :         $ hostnamectl set-hostname master
                          $ bash

                        
![image](https://github.com/user-attachments/assets/05101107-798b-4608-ac18-92e344f81cc7)


# Docker Installation Guide

Launch an EC2 instance and run the below Commands to install docker in linux based machine:

To update packages :		$ sudo yum update 

Install Docker: 		$ yum install docker

Enable docker:		$ systemctl enable docker

Restart docker:		$ systemctl restart docker

Check docker status: 		$ systemctl status docker

Check docker version:	$docker --version





