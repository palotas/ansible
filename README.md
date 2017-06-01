# ansible
ubuntu base image: allows for ssh access <br>
port forward 2222 to 22 (SSH) & 8080 8080 (Jenkins)

add authorized key from macbook to ubuntu machine: cat ~/.ssh/id_rsa.pub | ssh user@123.45.56.78 "mkdir -p ~/.ssh && cat >>  ~/.ssh/authorized_keys"

## set up ssh keys so that passphrase only needs to be entered once:
http://blog.packetdisarray.com/2015/08/06/passphrase-ssh-keys-without-repetitive-typing/

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

Delete license key: ~/.IntelliJIdea15/config/eval/idea15.evaluation.key

## install google chrome 
wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add - 
sudo sh -c 'echo "deb https://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google.list'
sudo apt-get update
sudo apt-get install google-chrome-stable

## start SONARQUBE docker container 
docker run -d --name sonarqube -p 9000:9000 -p 9092:9092 sonarqube

## start Jenkins docker container 
sudo docker run -p 8080:8080 -p 50000:50000 -v /home/e34/jenkins_home:/var/jenkins_home palotas/jenkins-cdi:0.1

## start Tomcat docker container
sudo docker run -it --rm -p 9999:8080 --expose=8080 --name=tomcatserver palotas/tomcat7.0-cdi:0.1 
- port 8080 needs to be exposed so the jenkins container can talk to tomcat container 
- the IP of tomcat container is 172.17.0.2, to check run sudo docker inspect e77e0bd0344d

## port config
- Jenkins: 8080
- Tomcat: 9999
- SonarQube: 9000


## attach to docker container 
docker exec -it containerIdOrName bash


Links: 
https://opensolitude.com/2015/05/26/building-docker-images-with-ansible.html




