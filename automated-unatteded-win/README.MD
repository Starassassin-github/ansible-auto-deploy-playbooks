# Automated Deploy windows in vCenter Cluster with Ansible
  
Automated deployment of windows in vCenter cluster The cluster can be an ESXi host or vCenter, but this repository is the cluster for vCenter. You just change the answer file to change the cluster to a specific IP address.


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
```

## First Step Build your own ISO
-  ***Custom ESXi Image:*** You can use other options; there are many ways to build your own ISO file, but I chose windowsafg.
    1.  Script file.
    2.  burn to ISO file.
    3.  Upload the ISO to your vCenter or ESXi host.

## Deploy

 1. First, you must have edit and setting your VM
    - 1.1 Edit cfg_win10pro_thin_vars.yml   
    - 1.2 Make sure you have a custom windows ISO installer in the vCenter Datastore and are ready to upload it.  
    - 1.3 run ```ansible-playbook vm_set_wins10pro_playbook.yml``` 
	    >vm_set_wins10pro_playbook.yml is a multiple VM.
	    >vm_windows10_pro_playbook.yml is a single VM. 
    - 1.4 wait and finish complete installer.


## Reference
1. https://docs.ansible.com/ansible/latest/collections/community/vmware/index.html#

## Thank you and Contributor
