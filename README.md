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
 
 
 


`192.168.24.137 ansiblemaster.lab.local`


* check that apache doesnt installed `rpm -qa httpd`


* get private key 
 - ssh-keygen
- Your identification has been saved in /home/nour/.ssh/id_rsa

--------------------------------------------------------------------------------------------------------------------------------------------------------------------
2- ## Master 
* sudo yum install python3
* sudo yum install epel-release
* sudo yum install ansible
* sudo yum install ansible-galaxy : if you want to Use ansible galaxy to download roles from GIT using URLs
* sudo yum install git
* vim /etc/hosts : add record of client `192.168.24.136 nourhan.lab.local`
* ssh-keygen
* ssh-copy-id -i /home/nour/.ssh/id_rsa.pub nour@192.168.24.136
* in  /etc/ansible/  `sudo vim key.pem`
* mkdir ansible-project 
* mkdir inventories/hosts : client  ansible_host=192.168.24.136  ansible_user=nour  ansible_ssh_private_key_file=/etc/ansible/key.pem
 
* mkdire roles : 2 dir one for apache role another for chrony role  
* 2 playbooks : ntp and httpd 
----------------------------------------------------------------------------------------------------------------------------
## result 



1- ![image](https://user-images.githubusercontent.com/125203973/224029220-be8b1f8a-dbb1-4540-bfea-a1d712f143d3.png)


2- ![image](https://user-images.githubusercontent.com/125203973/224029855-607114b3-9c54-4be6-8c6a-a07160d2c955.png)

3- ![image](https://user-images.githubusercontent.com/125203973/224029698-d958e0e6-da05-4ca3-91f4-b66910b10219.png)
 




4- ![image](https://user-images.githubusercontent.com/125203973/224029336-c9194672-ba6b-4771-9746-7c1f2dbe289c.png)

5-  ![image](https://user-images.githubusercontent.com/125203973/224029483-9ae61ed2-a27b-49d0-a52f-450d82cbfca6.png)

6- ![image](https://user-images.githubusercontent.com/125203973/224032105-fbf90dc6-5be6-47d4-b75d-08099f06b704.png)


 
 









