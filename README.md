# ansible
ubuntu base image: allows for ssh access <br>
port forward 2222 to 22 (SSH) & 8080 8080 (Jenkins)

add authorized key from macbook to ubuntu machine: cat ~/.ssh/id_rsa.pub | ssh e34@127.0.0.1 'umask 077; cat >>.ssh/authorized_keys'


execute ansible playbook: ansible-playbook myplaybook.yml --ask-become-pass

Links: 
https://opensolitude.com/2015/05/26/building-docker-images-with-ansible.html




