FROM ubuntu:18.04

ENV ROOT_PASS 'v245G5BrnZwUM'
ENV USER_NAME 'level7'
ENV USER_PASS "level7"
ENV FLAG '${CLUSIRceh2020|Ajg9sopQ}'

RUN export DEBIAN_FRONTEND=noninteractive
RUN apt-get update -y
RUN apt-get install -yq openssh-server sudo lua5.3
RUN mkdir /var/run/sshd
RUN echo "root:${ROOT_PASS}" | chpasswd
RUN useradd -m -d "/home/${USER_NAME}" ${USER_NAME} -s /usr/bin/lua5.3
RUN echo "${USER_NAME}:${USER_PASS}" | chpasswd
RUN sed -ri 's/^#?PermitRootLogin\s+.*/PermitRootLogin no/' /etc/ssh/sshd_config
RUN sed -ri 's/UsePAM yes/#UsePAM yes/g' /etc/ssh/sshd_config
RUN mkdir /root/.ssh
RUN echo "root ALL=(ALL) ALL" > /etc/sudoers && \
    echo "${USER_NAME} ALL = (root) NOPASSWD: /usr/bin/lua5.3" >> /etc/sudoers && \
    echo "" >> /etc/sudoers
RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN echo ${FLAG} > /root/flag
EXPOSE 22
CMD ["/usr/sbin/sshd", "-D"]
