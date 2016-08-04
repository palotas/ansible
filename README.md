# ansible
ubuntu base image: allows for ssh access <br>
port forward 2222 to 22 (SSH) & 8080 8080 (Jenkins)

add authorized key from macbook to ubuntu machine: cat ~/.ssh/id_rsa.pub | ssh user@123.45.56.78 "mkdir -p ~/.ssh && cat >>  ~/.ssh/authorized_keys"


# execute ansible playbook: 
ansible-playbook myplaybook.yml --ask-become-pass

# uninstall libre office form ubuntu machine
sudo apt-get remove --purge libreoffice* <br>
sudo apt-get clean <br>
sudo apt-get autoremove <br>

## set up IntelliJ
go to ~/idea.../bin <br>
execute: ./idea.sh (this starts IntelliJ) <br>
accept license agreement, import Seleniumtraining Git project etc. <br>
Tools -> Create Desktop Entry (create desktop entry) 

## install google chrome 
wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add - 
sudo sh -c 'echo "deb https://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google.list'
sudo apt-get update
sudo apt-get install google-chrome-stable

## start SONARQUBE docker container 
docker run -d --name sonarqube -p 9000:9000 -p 9092:9092 sonarqube

## start Jenkins docker container 
sudo docker run -p 8080:8080 -p 50000:50000 -v /home/e34/jenkins_home:/var/jenkins_home jenkins

Links: 
https://opensolitude.com/2015/05/26/building-docker-images-with-ansible.html




