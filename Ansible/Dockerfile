FROM ubuntu:18.04

RUN apt-get update; \
    apt-get install -y wget apt-transport-https software-properties-common; \
    wget -q https://packages.microsoft.com/config/ubuntu/20.04/packages-microsoft-prod.deb; \
    apt-get install ./packages-microsoft-prod.deb; \
    apt-get update; \
    apt-get install -y apt-utils; \
    apt-get install -y aptitude; \
    aptitude update; \
    aptitude install -y openssh-client; \
    aptitude install -y python3-pip; \
    aptitude install -y powershell; \
    aptitude clean; \
    apt-get clean

RUN pip3 install --upgrade pip; \
    aptitude install -y ansible
    pip3 install ansible[azure]
