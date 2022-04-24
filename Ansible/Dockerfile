
FROM ubuntu:18.04

RUN apt-get update; \
    apt install openssh-client; \
    apt install -y sshpass; \
    apt install nano; \
    apt install -y iputils-ping; \
    apt-get install -y wget apt-transport-https software-properties-common; \
    wget -q https://packages.microsoft.com/config/ubuntu/20.04/packages-microsoft-prod.deb; \
    apt-get install ./packages-microsoft-prod.deb; \
    apt-get update; \
    add-apt-repository universe; \
    apt install -y python3-pip; \
    apt install -y powershell; \
    pwsh -c "Set-PackageSource -Name PSGallery -Trusted"; \
    pwsh -c "Install-Module AZ -Scope AllUsers"; \
    apt install -y git; \
    apt-get clean

ENV LANG C.UTF-8
ENV LC_ALL C.UTF-8

RUN pip3 install --upgrade pip; \
    pip3 install "ansible==2.9.12"; \
    pip3 install ansible[azure]; \
    pip3 install pyvmomi; \
    pip3 install ansible-lint
