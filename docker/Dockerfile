# our local base image
FROM kalilinux/kali-rolling:amd64

LABEL description="Kali Container"

# install build dependencies 
RUN apt-get update && apt-get upgrade -q -y --force-yes && apt-get install -y sudo kali-tools-information-gathering kali-tools-passwords openvpn bash-completion net-tools metasploit-framework ghidra

#kali-tools-information-gathering
#kali-tools-vulnerability
#kali-tools-web
#kali-tools-database
#kali-tools-passwords
#kali-tools-wireless
#kali-tools-reverse-engineering
#kali-tools-exploitation
#kali-tools-social-engineering
#kali-tools-sniffing-spoofing
#kali-tools-post-exploitation
#kali-tools-forensics
#kali-tools-reporting

# configure SSH for communication with Visual Studio 
#RUN mkdir -p /var/run/sshd

#RUN echo 'PasswordAuthentication yes' >> /etc/ssh/sshd_config && \ 
#   ssh-keygen -A 

# expose port 22 
EXPOSE 22

# start ssh
#RUN service ssh start

#VOLUME /home/kali

# create user
RUN useradd -m -d /home/kali -s /bin/bash -G sudo kali
RUN mkdir -p /etc/sudoers.d/ && echo "kali ALL=(ALL : ALL) NOPASSWD:ALL" >> /etc/sudoers.d/username
USER kali

WORKDIR /home/kali

# start ssh
#ENTRYPOINT service ssh restart && bash
