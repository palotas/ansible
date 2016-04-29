# ansible
ubuntu base image: allows for ssh access <br>
port forward 2222 to 22 (SSH) & 8080 8080 (Jenkins)

add authorized key from macbook to ubuntu machine: cat ~/.ssh/id_rsa.pub | ssh user@123.45.56.78 "mkdir -p ~/.ssh && cat >>  ~/.ssh/authorized_keys"


# execute ansible playbook: 
ansible-playbook myplaybook.yml --ask-become-pass

# uninstall libre office form ubuntu machine
sudo apt-get remove --purge libreoffice*
sudo apt-get clean
sudo apt-get autoremove


Links: 
https://opensolitude.com/2015/05/26/building-docker-images-with-ansible.html




