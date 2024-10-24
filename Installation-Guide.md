Package Management :

The approack to installing Docker largely depends on the package manager for LInux Distribution. APT (ubuntu/Debian) and YUM for (red hat/Centos) are the two popular examples


Docker Installation Guide

Run the below Commands to install docker in linux based machine

Switch to root user : 		$ sudo -i

To update packages :		$ sudo yum update 

Install Docker: 		$ yum install docker

Enable docker:		$ systemctl enable docker

Restart docker:		$ systemctl restart docker

Check docker status: 		$ systemctl status docker

Check docker version:	$docker --version





