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

Install Docker: 		$ yum install docker -y

Enable docker:		$ systemctl enable docker

Restart docker:		$ systemctl restart docker

Check docker status: 		$ systemctl status docker

Check docker version:	$docker --version

# Kubernetes Installation Guide

To form Kubernetes Cluster, we need the machine to have conternerized mechanism, so docker needs to be installed before installing kubernetes cluster
validate:
- swap is in disabled state **free -mh**    -> To disable swap, sudo swapoff -a can be used to disable swapping temporarily.
- SELinux is in diabled status **sestatus**
- 
     # Set SELinux in permissive mode (effectively disabling it)
      $ sudo setenforce 0
       sudo sed -i 's/^SELINUX=enforcing$/SELINUX=permissive/' /etc/selinux/config

     # Installing kubeadm, kubelet and kubectl
       You will install these packages on all of your machines:

       **kubeadm:** the command to bootstrap the cluster.

      ** kubelet:** the component that runs on all of the machines in your cluster and does things like starting pods and containers.

       **kubectl:** the command line util to talk to your cluster.

     # Step 1: Add Kubernetes yum Repositoy - Copy paste the below command in cmd prompt where docker is installed earlier

        cat <<EOF | sudo tee /etc/yum.repos.d/kubernetes.repo
       [kubernetes]
        name=Kubernetes
        baseurl=https://pkgs.k8s.io/core:/stable:/v1.31/rpm/
        enabled=1
        gpgcheck=1
        gpgkey=https://pkgs.k8s.io/core:/stable:/v1.31/rpm/repodata/repomd.xml.key
        exclude=kubelet kubeadm kubectl cri-tools kubernetes-cni
        EOF

     # Step 2: Install kubelet, kubeadm and kubectl: 

        $ sudo yum install -y kubelet kubeadm kubectl --disableexcludes=kubernetes
  

     # Step 3: Enable Kubelet
          systemctl enable kubelet

          systemctl restart kubelet
  
     # Initialize kubeadm

          kubeadm init

       Caution: Error is because I have taken 1 CPU instance

    # Troubleshoot Error : Prerequisites for installing Kubernetes

             - 2 GB or more of RAM per machine (any less will leave little room for your apps).
             - 2 CPUs or more for control plane machines.
             - Full network connectivity between all machines in the cluster (public or private network is fine).
             - Unique hostname, MAC address, and product_uuid for every node. See here for more details.

             


        












