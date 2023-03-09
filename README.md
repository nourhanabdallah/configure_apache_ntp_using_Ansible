# configure_apache_ntp_using_Ansible


## requirements

* master 
* client 
* authenticate betwwen them passwordless 
* configure apache 
* configure ntp package 
* use roles 
------------------------------------------------------------------------------------------------------------------------------------------------------------
1- ## client 
* vim /etc/hosts

 add record of master 
192.168.24.140 client2.lab.local

192.168.24.137 ansiblemaster.lab.local


* check that apache doesnt installed `rpm -qa httpd`


* get private key 
 - ssh-keygen
- Your identification has been saved in /home/nour/.ssh/id_rsa

--------------------------------------------------------------------------------------------------------------------------------------------------------------------
2- ## Master 
* sudo yum install python3
* sudo yum install epel-release
* sudo yum install ansible
* sudo yum install ansible-galaxy :Use ansible galaxy to download roles from GIT using URLs
* sudo yum install git
* vim /etc/hosts : add record of client `192.168.24.140 client2.lab.local`
* ssh-keygen
* ssh-copy-id -i /home/nour/.ssh/id_rsa.pub nour@192.168.24.140
* in  /etc/ansible/  `sudo vim key.pem`
* 


