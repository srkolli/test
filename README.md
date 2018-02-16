# Information about this playbook

 This playbook sets up the basic components needed for Ruby on Rails (RoR) deployment. 
 To use the playbook :
  - First edit the "hosts" inventory file to include the hostnames of the machines on which you want these deployed.
  - Ensure that SSH keys are setup communication between the contrl machine and hosts you need this play book to run on.
  - Edit the group_vars/ror file to change any of RoR variables defined for this playbook.

# System Requirement
  - Ansible 1.2 or newer
  - Tested on Suse/Ubuntu/RHEL 

# Roles defined in this playbook 
  - See: roles/tomcat8/tasks/main.yml

# Steps to run the playbook
  - ansible-playbook -i hosts ror.yml

  The playbook should give a summary of what is installed and if they are working. Additional information like this is provided :

# Installation Path , log location and startup commands

  - Install Location 
  - Log Location 
  - Port
  - start/stop commands and information about the user they should be run as
  - application account and password 
  - sudoers entry ( that needs to be done manually ??) 
    Add below sudo entry in /etc/sudoers file 
    admin-ror ALL=(ALL) NOPASSWD: /etc/init.d/tomcatd*, /usr/bin/lsof
  - Application Installation path , config file and applogs

# References to any Security recommendations for hardening
 