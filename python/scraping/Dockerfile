FROM python:3

MAINTAINER Naruhiko

# Japanese Localization
RUN cp /usr/share/zoneinfo/Asia/Tokyo /etc/localtime

# User settings
ARG UID=1000
ARG USER=ユーザー名
RUN useradd -m -u ${UID} ${USER}
# Change user
USER ${UID}

# python package
RUN pip install --upgrade pip && \
pip install requests && \
pip install bs4
