# ubuntu-autoinstall

An Ansible Playbook that performs unattended Ubuntu Server 20.04 VM installations on VMware vSphere.

## Prerequisites

Prepare an Ubuntu machine as Ansible Controller by running the following commands:

* ```sudo apt update && sudo apt install python3 python3-pip git xorriso```
* ```git clone https://github.com/rutgerblom/ubuntu-autoinstall.git ~/git/ubuntu-autoinstall```
* ```pip3 install --upgrade -r ~/git/ubuntu-autoinstall/pip_requirements.txt```
* ```ansible-galaxy collection install --upgrade -r ~/git/ubuntu-autoinstall/requirements.yml```

## Usage

Copy the ```variables_sample.yml``` file to ```variables.yml``` and modify the settings so that they match your environment and your requirements. Start the Ubuntu Server deployment by running: ```ansible-playbook DeployUbuntu.yml```

# Automated Deploy ubuntu in vCenter Cluster with Ansible
  
Automated deployment of ubuntu in vCenter cluster The cluster can be an ESXi host or vCenter, but this repository is the cluster for vCenter. You just change the answer file to change the cluster to a specific IP address.


# Prerequisite

1. Creating an Unattended Install of Windows
2. Virtual Machine
3. Ansible Playground to deployed
4. Custom ISO Image
5. Ansible Community.Vmware basic

# Prerequisite-installer


```
Ansible:                2.9.10
Python :				3.10
Pyvmomi:                7.0
xorrisofs:				x.x
```

## First Step Build your own ISO
-  ***Custom ESXi Image:*** You can use other options; there are many ways to build your own ISO file.

## Deploy

 1. First, you must have edit and setting your VM
    - 1.1 Edit cfg_ubuntu20.yml  
    - 1.2 Make sure you have a custom ubuntu ISO installer in the ansible workspace and are ready to create custom iso it.  
    - 1.3 run ```ansible-playbook vm_easycreate_ubuntu20server_playbook.yml``` 
	    >vm_easycreate_ubuntu20server_playbook.yml is a multiple VM contain cfg_ubuntu20.yml 
    - 1.4 wait and finish complete installer.


## Reference
1. https://github.com/rutgerblom/ubuntu-autoinstall
## Thank you and Contributor
