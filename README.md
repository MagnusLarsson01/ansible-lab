# ansible-lab
Lab environment for Ansible


## Prerequisits
Create a folder in you home directory named ansible-lab  
Add the following subdirectories:  
shared  
ssh/control_node  
ssh/ubuntu-a  
ssh/ubuntu-b  
ssh/ubuntu-c  
ssh/ubuntu-d  

Download/clone the repository  

Start the lab environment by running (in the ansible-lab directory) command:  
docker-compose up -d --build  

Enter the control node:   
docker exec -it controlnode /bin/bash

su - ansible  

At first run, setup ssh:  
ansible> ssh-keygen  

ssh-copy-id ubuntu-a.labnet.io etc. for each managed node  

Shut down the lab environment:  
docker-compose down  