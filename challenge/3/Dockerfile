FROM ubuntu:18.04

ENV ROOT_PASS 'E8h957wHcwM5Vx'
ENV USER_NAME 'level3'
ENV USER_PASS "level3"
ENV FLAG '${CLUSIRceh2020|tionseU}'
ENV PARAM1 "COLLECTOR_AUTH"
ENV VALUE1 "root:RThoOTU3d0hjd001Vng="

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
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/df" >> /etc/sudoers && \
    echo "" >> /etc/sudoers
RUN echo "export ${PARAM1}=${VALUE1}" >> "/home/${USER_NAME}/.bashrc"
RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN echo ${FLAG} > /root/flag
EXPOSE 22
ENTRYPOINT /usr/sbin/sshd -D && cron start 
