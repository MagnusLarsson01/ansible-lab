FROM ubuntu:18.04
# RUN apt update -y && apt install software-properties-common -y && apt-add-repository ppa:ansible/ansible && apt install ansible -y
RUN apt update && apt install software-properties-common -y && apt-add-repository --yes --update ppa:ansible/ansible && apt install ansible -y 
RUN useradd ansible 
# && echo "password" | passwd --stdin ansible && echo "ansible ALL=(ALL) NOPASSWD:ALL" > /etc/sudoers.d/ansible
# COPY ansible /var/ans/
WORKDIR /var/ans