FROM node:8.16

ARG USERNAME=user
ARG PASSWORD=user
ARG PORT=8888

RUN apt-get update && \
    apt-get install -y sudo vim

RUN adduser --disabled-password --gecos "" $USERNAME && \
    echo "$USERNAME:$PASSWORD" | chpasswd


WORKDIR /home/$USERNAME

EXPOSE $PORT
ENTRYPOINT /bin/bash
