# vim:set ft=dockerfile:

#BASE image : ubuntu20.04 + asterisk 20.1.0 + nodejs 18.12.0 + typescript 4.9.2 with mongo realtime backend pathched
FROM ubuntu:20.04

LABEL maintainer="GeonhaPark"

ARG DEBIAN_FRONTEND=noninteractive
ENV TZ=Asia/Seoul
# 만들 이미지에 작업할 디렉토리로 이동합니다. 
# WORKDIR /ari
# 현재 디렉토리에 package로 시작하는 파일들을 복사하여 이미지에서 작업할 디렉토리로 복사합니다. 
# COPY package*.json /ari/
# 이미지 디렉토리에서 npm install 명령어를 실행해 줍니다. 
RUN apt-get update && apt-get install -y tzdata
RUN apt-get install -y -qq --no-install-recommends --no-install-suggests \
    gcc \
    g++ \
    make \
    cmake \
    wget \
    curl \
    git  \
    vim  \
    net-tools  \
    iputils-ping  \
    openssh-server 

RUN apt-get install sudo -y

# Create a new user with a password
RUN useradd -m hanulso && echo "hanulso:hanulso" | chpasswd
RUN usermod -aG sudo hanulso
# Specify that commands should run as this user
USER root
RUN chsh -s /bin/bash hanulso

# 현재 폴더에 있는 모든 파일들을 복사하여 이미지 디렉토리에 복사합니다. 
# 여기과정이 자신이 작성한 코드 등 리소스들이 복사됩니다
# COPY . .

#port 연결
# EXPOSE  5060:5060/udp \
#     5060:5060/tcp \
#     8088:8088/tcp \
#     8089:8089/tcp 

#volume 연결
# VOLUME /var/lib/asterisk/sounds \
#     /var/lib/asterisk/keys \
#     /var/lib/asterisk/phoneprov \
#     /var/spool/asterisk \
#     /var/log/asterisk \
#     /var/lib/asterisk/moh \
#     /etc/asterisk

COPY docker-entrypoint.sh .
ENTRYPOINT ["./docker-entrypoint.sh"]
CMD ["/bin/bash"]

