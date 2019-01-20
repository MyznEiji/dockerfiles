# docker build -t dockerfile-checker .


# ubuntu16.04を使う
FROM  ubuntu:16.04

# apt-get update
RUN apt-get -y update && apt-get install -y curl vim

# Install Linttool of Dockerfile
RUN cd && curl -L -O https://github.com/hadolint/hadolint/releases/download/v1.15.0/hadolint-Linux-x86_64

# add alias 
RUN echo "alias check='~/hadolint-Linux-x86_64'" >> ~/.bashrc

# Permission
RUN chmod +x ~/hadolint-Linux-x86_64

# Source コマンドを使えるようにする
RUN mv /bin/sh /bin/sh_tmp && ln -s /bin/bash /bin/sh

# Sorce
RUN source ~/.bashrc

# Sorceコマンドを使えるようにするための設定をリセット
RUN rm /bin/sh && mv /bin/sh_tmp /bin/sh


