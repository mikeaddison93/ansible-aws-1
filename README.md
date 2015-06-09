# Creating AWS Instances with Ansible

*Scripts* for [Ansible](http://www.ansible.com) that creates an AWS instance, executes something inside, deletes the instance.

Tested for Ubuntu based instances.

### Usage

This [Ansible](http://www.ansible.com) playbook will create a specified instance:

* creates the AWS instance and wait for it to be ready (SSH available)
* uploads a public SSH key as specified so that user "ubuntu" can log without password
* executes something in the instance (to be defined)
* deletes the same instance


```
## install prerequisites ##
# in Ubuntu/Debian
user@host:~$ sudo apt-get install python-pip
user@host:~$ sudo apt-get install python-passlib
user@host:~$ sudo pip install ansible
user@host:~$ sudo pip install --upgrade ansible

## clone this script and configure for your target hosts ##
user@host:~$ git clone <this repo>
user@host:~$ cd ansible-aws
user@host:~/ansible-aws$ cp group_vars/all.sample group_vars/all
user@host:~/ansible-aws$ nano group_vars/all

## run Ansible playbook
user@host:~/secure-ssh$ ansible-playbook -i hosts bootstrap.yml
```

### Reference

* [Ansible](http://www.ansible.com/)

### Contact

* Author: [BlueWind] Stefano Costa (http://www.bluewind.it)
* Email: stefano DOT costa AT bluewind DOT it

