# root vao ssh
```
RUN apk add --no-cache openssh
RUN echo "root:12345" | chpasswd && \
    sed -i 's/#PermitRootLogin.*/PermitRootLogin yes/' /etc/ssh/sshd_config
RUN ssh-keygen -A
EXPOSE 22
CMD ["/usr/sbin/sshd", "-D"]
```
