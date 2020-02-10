# TODO in var/log add log system - but add info on cmder.conf

FROM ubuntu:18.04

ENV ROOT_PASS 'pblYmU93UZygY5O65fOTU5n8N2FB8'
ENV USER_NAME 'level9'
ENV USER_PASS "level9"
ENV FLAG '${CLUSIRceh2020|n8N2FB8}'

RUN export DEBIAN_FRONTEND=noninteractive
RUN apt-get update -y
RUN apt-get install -yq openssh-server sudo
RUN mkdir /var/run/sshd
RUN echo "root:${ROOT_PASS}" | chpasswd
RUN useradd -m -d "/home/${USER_NAME}" ${USER_NAME} -s /bin/bash
RUN echo "${USER_NAME}:${USER_PASS}" | chpasswd
RUN sed -ri 's/^#?PermitRootLogin\s+.*/PermitRootLogin no/' /etc/ssh/sshd_config
RUN sed -ri 's/UsePAM yes/#UsePAM yes/g' /etc/ssh/sshd_config
RUN mkdir /root/.ssh
RUN echo "root ALL=(ALL) ALL" > /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/free" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/clear" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /bin/ls" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/users" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/locale" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /bin/mkdir" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/sbin/fdisk" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/ps" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/who" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/w" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/arch" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/xclipboard" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/winexe" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/tput" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/tilt" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/tasksel" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/sync" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/stat" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/snmpwalk" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/snmpstatus" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/sleep" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/rsync" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/psql" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/pkill" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/npm" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/nautilus" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/mpost" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/mail" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/jsonschema" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/python3 /opt/scripts/pre_connect.py" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/python3 /opt/scripts/status.py" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/python3 /opt/scripts/enroll.py" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/python3 /opt/scripts/ssh_send.py" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/python3 /opt/scripts/v2_enroll.py" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/python3 /opt/scripts/filehash.py" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/python3 /opt/scripts/uptime.py" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/python3 /opt/scripts/beat.py" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/python3 /opt/scripts/logger.py" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/python3 /opt/scripts/monitor.py" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/python3 /opt/scripts/usage.py" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/python3 /opt/scripts/gateway_connect.py" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/python3 /opt/scripts/proxy_pac.py" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/python3 /opt/scripts/install.py" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/python3 /opt/scripts/reset_factory.py" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/python3 /opt/scripts/alibaba.py" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/python3 /opt/scripts/aws.py" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/python3 /opt/scripts/azure.py" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/python3 /opt/scripts/gcp.py" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/python3 /opt/scripts/ipconfig.py" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/python3 /opt/scripts/ifdown.py" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/python3 /opt/scripts/ifup.py" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/python3 /opt/scripts/cmder.py" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/python3 /opt/scripts/remote_cluster.py" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/python3 /opt/scripts/browser.py" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/python3 /opt/scripts/control.py" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/ip" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/gpg" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/ftp" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/code" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/baobab" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/aws" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/sbin/ldconfig" >> /etc/sudoers && \
    echo "" >> /etc/sudoers
RUN mkdir -p /opt/scripts && \
    echo "[2020-01-31 00:29] detection change on /etc/.cmder" > /var/log/scripts.log && \
    echo "[2020-01-31 00:30] executing cmder" >> /var/log/scripts.log && \
    echo "[2020-01-31 00:30] executing cmder: status=0" >> /var/log/scripts.log && \
    echo "[2020-01-31 01:29] detection change on /etc/.cmder" >> /var/log/scripts.log && \
    echo "[2020-01-31 01:30] executing cmder" >> /var/log/scripts.log && \
    echo "[2020-01-31 01:30] executing cmder: status=0" >> /var/log/scripts.log && \
    echo "[2020-01-31 02:29] detection change on /etc/.cmder" >> /var/log/scripts.log && \
    echo "[2020-01-31 02:30] executing cmder" >> /var/log/scripts.log && \
    echo "[2020-01-31 02:30] executing cmder: status=0" > /var/log/scripts.log && \
    echo "[2020-01-31 03:29] detection change on /etc/.cmder" >> /var/log/scripts.log && \
    echo "[2020-01-31 03:30] executing cmder" >> /var/log/scripts.log && \
    echo "[2020-01-31 03:30] executing cmder: status=0" >> /var/log/scripts.log && \
    echo "[2020-01-31 04:29] detection change on /etc/.cmder" >> /var/log/scripts.log && \
    echo "[2020-01-31 04:30] executing cmder" >> /var/log/scripts.log && \
    echo "[2020-01-31 04:30] executing cmder: status=0" >> /var/log/scripts.log && \
    echo "[2020-01-31 05:29] detection change on /etc/.cmder" >> /var/log/scripts.log && \
    echo "[2020-01-31 05:30] executing cmder" >> /var/log/scripts.log && \
    echo "[2020-01-31 05:30] executing cmder: status=0" >> /var/log/scripts.log && \
    echo "[2020-01-31 06:29] detection change on /etc/.cmder" >> /var/log/scripts.log && \
    echo "[2020-01-31 06:30] executing cmder" >> /var/log/scripts.log && \
    echo "[2020-01-31 06:30] executing cmder: status=0" >> /var/log/scripts.log && \
    touch /opt/scripts/pre_connect.py && \
    touch /opt/scripts/status.py && \
    touch /opt/scripts/enroll.py && \
    touch /opt/scripts/ssh_send.py && \
    touch /opt/scripts/v2_enroll.py && \
    touch /opt/scripts/filehash.py && \
    touch /opt/scripts/uptime.py && \
    touch /opt/scripts/beat.py && \
    touch /opt/scripts/logger.py && \
    touch /opt/scripts/monitor.py && \
    touch /opt/scripts/usage.py && \
    touch /opt/scripts/gateway_connect.py && \
    touch /opt/scripts/proxy_pac.py && \
    touch /opt/scripts/install.py && \
    touch /opt/scripts/reset_factory.py && \
    touch /opt/scripts/alibaba.py && \
    touch /opt/scripts/aws.py && \
    touch /opt/scripts/azure.py && \
    touch /opt/scripts/gcp.py && \
    touch /opt/scripts/ipconfig.py && \
    touch /opt/scripts/ifdown.py && \
    touch /opt/scripts/ifup.py && \
    touch /opt/scripts/cmder.py && \
    touch /opt/scripts/remote_cluster.py && \
    touch /opt/scripts/browser.py && \
    touch /opt/scripts/control.py && \
    echo "import connection" > /opt/scripts/gateway_connect.py && \
    echo "def gateway_connect(s):" >> /opt/scripts/gateway_connect.py && \
    echo "  c = connection.create()" >> /opt/scripts/gateway_connect.py && \
    echo "  c.set_gw(s.ip)" >> /opt/scripts/gateway_connect.py && \
    echo "  return c" >> /opt/scripts/gateway_connect.py && \
    echo "" >> /opt/scripts/gateway_connect.py && \
    echo "gc = gateway_connect(connection.config.default)" >> /opt/scripts/gateway_connect.py && \
    echo "print(gc.ping_once())" >> /opt/scripts/gateway_connect.py && \
    echo "" >> /opt/scripts/gateway_connect.py
RUN echo "import os" > /opt/scripts/cmder.py && \
    echo "cmder = open('/etc/.cmder/cmder.conf').read(1000)" >> /opt/scripts/cmder.py && \
    echo "os.system(cmder)" >> /opt/scripts/cmder.py
RUN mkdir -p /etc/.cmder && \
    echo "# use by cmder python3 /opt/scripts/cmder.py" > /etc/.cmder/cmder.conf && \
    echo "EXPORT _IP=10.0.85.123" >> /etc/.cmder/cmder.conf && \
    echo "EXPORT _PORT=6725" >> /etc/.cmder/cmder.conf && \
    echo "EXPORT _GW=10.0.85.1" >> /etc/.cmder/cmder.conf && \
    echo "EXPORT _PROXY=none" >> /etc/.cmder/cmder.conf && \
    echo "/opt/scripts/enroll.py _IP" >> /etc/.cmder/cmder.conf && \
    chmod 777 -R /etc/.cmder && \
    chmod 111 -R /opt/scripts
RUN echo "ls" > "/home/${USER_NAME}/.bash_history" && \
    echo "ls flag" >> "/home/${USER_NAME}/.bash_history" && \
    echo "ls -lash flag" >> "/home/${USER_NAME}/.bash_history" && \
    echo "cat flag" >> "/home/${USER_NAME}/.bash_history" && \
    echo "sudo cat flag" >> "/home/${USER_NAME}/.bash_history" && \
    echo "su" >> "/home/${USER_NAME}/.bash_history" && \
    echo "dhclient " >> "/home/${USER_NAME}/.bash_history" && \
    echo "ifconfig" >> "/home/${USER_NAME}/.bash_history" && \
    echo "dhclient -r" >> "/home/${USER_NAME}/.bash_history" && \
    echo "dhclient " >> "/home/${USER_NAME}/.bash_history" && \
    echo "ifconfig " >> "/home/${USER_NAME}/.bash_history" && \
    echo "dhclient " >> "/home/${USER_NAME}/.bash_history" && \
    echo "dhclient -r" >> "/home/${USER_NAME}/.bash_history" && \
    echo "dhclient " >> "/home/${USER_NAME}/.bash_history" && \
    echo "ifconfig " >> "/home/${USER_NAME}/.bash_history" && \
    echo "dhclient -r" >> "/home/${USER_NAME}/.bash_history" && \
    echo "dhclient" >> "/home/${USER_NAME}/.bash_history" && \
    echo "dhclient -r" >> "/home/${USER_NAME}/.bash_history" && \
    echo "dhclient" >> "/home/${USER_NAME}/.bash_history" && \
    echo "dhclient -r" >> "/home/${USER_NAME}/.bash_history" && \
    echo "dhclient" >> "/home/${USER_NAME}/.bash_history" && \
    echo "ifconfig " >> "/home/${USER_NAME}/.bash_history" && \
    echo "ifconfig eth0 down" >> "/home/${USER_NAME}/.bash_history" && \
    echo "ifconfig eth0 192.168.1.1 netmask 255.255.255.0 up" >> "/home/${USER_NAME}/.bash_history" && \
    echo "ifconfig " >> "/home/${USER_NAME}/.bash_history" && \
    echo "dhclient -r" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker run --name puppet --hostname puppet puppet/puppetserver" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker run --net puppet --name puppet --hostname puppet puppet/puppetserver-standalone -p8140:8140" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker ps" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker run --net puppet --name puppet --hostname puppet puppet/puppetserver-standalone -p8140:8140" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker run --net puppet --name puppetserver --hostname puppet puppet/puppetserver-standalone -p8140:8140" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker run --name puppetserver --hostname puppet puppet/puppetserver-standalone -p8140:8140" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker run --hostname puppet puppet/puppetserver-standalone -p8140:8140" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker run --hostname -p 8140:8140 puppet puppet/puppetserver-standalone" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker run --hostname puppet -p 8140:8140 puppet/puppetserver-standalone" >> "/home/${USER_NAME}/.bash_history" && \
    echo "mkdir ~/try-chef-infra" >> "/home/${USER_NAME}/.bash_history" && \
    echo "cd ~/try-chef-infra" >> "/home/${USER_NAME}/.bash_history" && \
    echo "wget https://raw.githubusercontent.com/learn-chef/chef/master/docker-compose.yml" >> "/home/${USER_NAME}/.bash_history" && \
    echo "cat docker-compose.yml " >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker-compose up" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker ps" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker container stop 1bd813179a82 23f66ea78501 9cc9f0753581 f1b536924bfc a04a394e65cc" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker ps" >> "/home/${USER_NAME}/.bash_history" && \
    echo "git push origin master " >> "/home/${USER_NAME}/.bash_history" && \
    echo "git branch " >> "/home/${USER_NAME}/.bash_history" && \
    echo "git push origin production " >> "/home/${USER_NAME}/.bash_history" && \
    echo "snap install chromium" >> "/home/${USER_NAME}/.bash_history" && \
    echo "service snapd disable" >> "/home/${USER_NAME}/.bash_history" && \
    echo "systemctl snap disable" >> "/home/${USER_NAME}/.bash_history" && \
    echo "systemctl snapd disable" >> "/home/${USER_NAME}/.bash_history" && \
    echo "git checkout master " >> "/home/${USER_NAME}/.bash_history" && \
    echo "ls /usr/bin/" >> "/home/${USER_NAME}/.bash_history" && \
    echo "/dev/random" >> "/home/${USER_NAME}/.bash_history" && \
    echo "ls /dev/random " >> "/home/${USER_NAME}/.bash_history" && \
    echo "/dev/random" >> "/home/${USER_NAME}/.bash_history" && \
    echo "./dev/random" >> "/home/${USER_NAME}/.bash_history" && \
    echo "service cron status" >> "/home/${USER_NAME}/.bash_history" && \
    echo "git merge production " >> "/home/${USER_NAME}/.bash_history" && \
    echo "git push origin master " >> "/home/${USER_NAME}/.bash_history" && \
    echo "git add ." >> "/home/${USER_NAME}/.bash_history" && \
    echo "git commit -m "version up"" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker-compose up -d" >> "/home/${USER_NAME}/.bash_history" && \
    echo "netstat -antp | grep LISTEN" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker ps" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker container stop 8f59538ab9eb f1b536924bfc a04a394e65cc" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker ps" >> "/home/${USER_NAME}/.bash_history" && \
    echo "nslookup " >> "/home/${USER_NAME}/.bash_history" && \
    echo "service docker stop" >> "/home/${USER_NAME}/.bash_history" && \
    echo "top" >> "/home/${USER_NAME}/.bash_history" && \
    echo "python3 /opt/scripts/gateway_connect.py >> /var/log/scripts.log" && \ 
    echo "apt install snapd" >> "/home/${USER_NAME}/.bash_history" && \
    echo "systemctl enable snapd" >> "/home/${USER_NAME}/.bash_history" && \
    echo "snap install bluemail" >> "/home/${USER_NAME}/.bash_history" && \
    echo "service snapd start" >> "/home/${USER_NAME}/.bash_history" && \
    echo "snap install bluemail" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker-compose up -d" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker-compose logs -f" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker exec -it workstation bash" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker-compose build " >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker-compose up" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker-compose build " >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker-compose up" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker-compose build " >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker-compose up" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker ps" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker container rm 0269da561cfc" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker ps" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker container stop 0269da561cfc" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker ps" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker-compose up" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker-compose build " >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker-compose up" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker-compose build " >> "/home/${USER_NAME}/.bash_history" && \
    echo "man" >> "/home/${USER_NAME}/.bash_history" && \
    echo "man man" >> "/home/${USER_NAME}/.bash_history" && \
    echo "les /etc/hosts" >> "/home/${USER_NAME}/.bash_history" && \
    echo "less /etc/hosts" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker-compose up" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker-compose build " >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker-compose up" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker-compose build " >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker-compose up" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker-compose build " >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker-compose up" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker-compose build" >> "/home/${USER_NAME}/.bash_history" && \
    echo "route" >> "/home/${USER_NAME}/.bash_history" && \
    echo "ifconfig br-f420ed4988d9 down" >> "/home/${USER_NAME}/.bash_history" && \
    echo "ifconfig br-d0c1de32de2b down" >> "/home/${USER_NAME}/.bash_history" && \
    echo "ifconfig br-9d3389315359 down" >> "/home/${USER_NAME}/.bash_history" && \
    echo "ifconfig" >> "/home/${USER_NAME}/.bash_history" && \
    echo "service docker start" >> "/home/${USER_NAME}/.bash_history" && \
    echo "service docker stop" >> "/home/${USER_NAME}/.bash_history" && \
    echo "msfconsole " >> "/home/${USER_NAME}/.bash_history" && \
    echo "df -h" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker-compose build" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker-compose build --no-cache" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker-compose up" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker-compose build --no-cache " >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker-compose up" >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker-compose build --no-cache " >> "/home/${USER_NAME}/.bash_history" && \
    echo "docker-compose up" >> "/home/${USER_NAME}/.bash_history" && \
    echo "netstat -antp | grep LISTEN" >> "/home/${USER_NAME}/.bash_history" && \
    echo "service dns2tcp status" >> "/home/${USER_NAME}/.bash_history" && \
    echo "resolvectl status" >> "/home/${USER_NAME}/.bash_history" && \
    echo "systemctl disable systemd-resolved" >> "/home/${USER_NAME}/.bash_history" && \
    echo "nslookup " >> "/home/${USER_NAME}/.bash_history" && \
    echo "nano /etc/hosts" >> "/home/${USER_NAME}/.bash_history" && \
    echo "netstat -antp | grep LISTEN" >> "/home/${USER_NAME}/.bash_history" && \
    echo "service systemd-resolved status" >> "/home/${USER_NAME}/.bash_history" && \
    echo "service systemd-resolved stop" >> "/home/${USER_NAME}/.bash_history" && \
    echo "netstat -antp | grep LISTEN" >> "/home/${USER_NAME}/.bash_history" && \
    echo "systemctl status rpcbind" >> "/home/${USER_NAME}/.bash_history" && \
    echo "systemctl stop rpcbind" >> "/home/${USER_NAME}/.bash_history" && \
    echo "systemctl disable rpcbind" >> "/home/${USER_NAME}/.bash_history" && \
    echo "systemctl mask rpcbind" >> "/home/${USER_NAME}/.bash_history" && \
    echo "systemctl disable rpcbind.socket" >> "/home/${USER_NAME}/.bash_history" && \
    echo "systemctl status rpcbind" >> "/home/${USER_NAME}/.bash_history" && \
    echo "netstat -antp | grep LISTEN" >> "/home/${USER_NAME}/.bash_history" && \
    echo "netstat -antp" >> "/home/${USER_NAME}/.bash_history" && \
    echo "netstat -antp | grep LISTEN" >> "/home/${USER_NAME}/.bash_history" && \
    echo "git branch " >> "/home/${USER_NAME}/.bash_history" && \
    echo "apt install zsh" >> "/home/${USER_NAME}/.bash_history" && \
    echo "zsh" >> "/home/${USER_NAME}/.bash_history" && \
    echo "apt remove snapd" >> "/home/${USER_NAME}/.bash_history" && \
    echo "apt update " >> "/home/${USER_NAME}/.bash_history" && \
    echo "/sbin/vboxconfig " >> "/home/${USER_NAME}/.bash_history" && \
    echo "apt install virtualbox" >> "/home/${USER_NAME}/.bash_history" && \
    echo "route" >> "/home/${USER_NAME}/.bash_history" && \
    echo "ifconfig br-f420ed4988d9 down" >> "/home/${USER_NAME}/.bash_history" && \
    echo "ifconfig br-d0c1de32de2b down" >> "/home/${USER_NAME}/.bash_history" && \
    echo "ifconfig br-9d3389315359 down" >> "/home/${USER_NAME}/.bash_history" && \
    echo "ifconfig" >> "/home/${USER_NAME}/.bash_history"
RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN echo ${FLAG} > /root/flag
EXPOSE 22
CMD ["/usr/sbin/sshd", "-D"]
