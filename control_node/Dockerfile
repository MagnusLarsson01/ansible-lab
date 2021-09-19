FROM ubuntu:18.04
RUN apt update \
    && apt install software-properties-common -y \
    && apt-get install -y python3-pip python3-dev \
    && apt-get -y install sudo \
    && cd /usr/local/bin \
    && ln -s /usr/bin/python3 python \
    && pip3 install --upgrade pip \
    && apt-add-repository --yes --update ppa:ansible/ansible && apt install ansible -y 

RUN useradd -m ansible -s /bin/bash && echo "ansible:password1" | chpasswd && usermod -aG sudo ansible 
RUN mkdir -p /home/ansible/.ssh
RUN chown -R ansible:ansible /home/ansible/.ssh
COPY hosts /etc/ansible/hosts
RUN mkdir /shared && mkdir /config
# Add a /shared volume
VOLUME ["/shared", "/config"]

WORKDIR /var/ans