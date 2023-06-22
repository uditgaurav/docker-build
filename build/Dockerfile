FROM ubuntu:16.04

RUN apt-get update && apt-get install -y sudo

# Add a user with sudo privileges
RUN useradd -ms /bin/bash myuser && echo "myuser:password" | chpasswd && adduser myuser sudo

USER myuser

CMD ["/bin/bash"]
