FROM ubuntu:18.04

ENV ROOT_PASS 'B8h956wHcwM5Vx'
ENV USER_NAME 'level1'
ENV USER_PASS "level1"
ENV FLAG '${CLUSIRceh2020|daLoiRa}'

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
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/sbin/ldconfig" >> /etc/sudoers && \
    echo "" >> /etc/sudoers
RUN echo "ls" > "/home/${USER_NAME}/.bash_history" && \
    echo "ls flag" >> "/home/${USER_NAME}/.bash_history" && \
    echo "ls -lash flag" >> "/home/${USER_NAME}/.bash_history" && \
    echo "cat flag" >> "/home/${USER_NAME}/.bash_history" && \
    echo "sudo cat flag" >> "/home/${USER_NAME}/.bash_history" && \
    echo "suu" >> "/home/${USER_NAME}/.bash_history" && \
    echo "${ROOT_PASS}" >> "/home/${USER_NAME}/.bash_history" && \
    echo "su" >> "/home/${USER_NAME}/.bash_history"
RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN echo ${FLAG} > /root/flag
EXPOSE 22
CMD ["/usr/sbin/sshd", "-D"]
