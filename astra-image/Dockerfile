FROM sogimu/astralinux:1.6
LABEL Сборка Astra Linux для Быданова Артёма
ADD ./files/ ./etc/apt/ && ./python/ ./home/user/
#ADD ./python/ ./home/user/
#COPY ./files/sources.list /etc/apt/
RUN apt-get update && apt-get install -y \
        qt5-default mono-dev squashfs-tools python \
        cmake zip tar git subversion smbclient curl \
        java-common default-jre openjdk-8-jdk openjdk-8-jdk-headless \
        openjdk-8-jre openjdk-8-jre-headless default-libmysqlclient-dev \
        && rm -rf /var/lib/apt/lists/*
RUN /home/user/Python-3.10.2/configure --enable-optimizations
CMD ["/bin/bash"]