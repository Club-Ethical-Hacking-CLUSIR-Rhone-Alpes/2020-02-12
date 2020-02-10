FROM ubuntu:18.04

ENV ROOT_PASS 'Az9X4Z256VJ7T'
ENV USER_NAME 'level6'
ENV USER_PASS "level6"
ENV FLAG '${CLUSIRceh2020|GenTBOB}'

RUN export DEBIAN_FRONTEND=noninteractive
RUN apt-get update -y
RUN apt-get install -yq openssh-server sudo nano
RUN mkdir /var/run/sshd
RUN echo "root:${ROOT_PASS}" | chpasswd
RUN useradd -m -d "/home/${USER_NAME}" ${USER_NAME} -s /bin/bash
RUN echo "${USER_NAME}:${USER_PASS}" | chpasswd
RUN sed -ri 's/^#?PermitRootLogin\s+.*/PermitRootLogin no/' /etc/ssh/sshd_config
RUN sed -ri 's/UsePAM yes/#UsePAM yes/g' /etc/ssh/sshd_config
RUN mkdir /root/.ssh && mkdir -p /var/www/html
RUN echo "root ALL=(ALL) ALL" > /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/free" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/clear" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /bin/nano /var/www/*" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /bin/ls" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/users" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/locale" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /bin/mkdir" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/who" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/w" >> /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/arch" >> /etc/sudoers && \
    echo "" >> /etc/sudoers
RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN echo ${FLAG} > /root/flag
EXPOSE 22
CMD ["/usr/sbin/sshd", "-D"]
