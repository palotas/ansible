# ansible
TODO: port forward 2222 to 22 (SSH)

If needed: add authorized key from macbook to ubuntu machine: ``cat ~/.ssh/id_rsa.pub | ssh e34@127.0.0.1 "mkdir -p ~/.ssh && cat >>  ~/.ssh/authorized_keys"`

SSH with: ssh -p 2222 e34@127.0.0.1

*hosts: training-vm*

-> is set to port 2222 on host to forward to 22 on VM 

-> set the default host in /etc/ansible/hosts 


## set up ssh keys so that passphrase only needs to be entered once:
http://blog.packetdisarray.com/2015/08/06/passphrase-ssh-keys-without-repetitive-typing/

## execute ansible playbook: 
``ansible-playbook e34-training-vm.yml browsers.yml docker.yml --extra-vars "ansible_become_pass=11"``

# uninstall libre office form ubuntu machine
``sudo apt-get remove --purge libreoffice* 
  sudo apt-get clean 
  sudo apt-get autoremove ``



## port config
- jenkins: 8080
- tomcat-QA: 9999
- tomcat-PROD: 9998
- SonarQube: 9000


Links: 
https://opensolitude.com/2015/05/26/building-docker-images-with-ansible.html




