FROM dcksv-linux-repo.kronshtadt.ru:5000/sogimi-astralinux-1.6:v1
LABEL Сборка Astra Linux для Быданова Артёма
COPY ./files/ ./etc/apt/
ADD ./python/ ./home/user/
#COPY ./files/sources.list /etc/apt/
RUN apt-get update && apt-get install -y \
        qt5-default mono-dev squashfs-tools python \
        cmake zip tar git subversion smbclient curl \
        java-common default-jre openjdk-8-jdk openjdk-8-jdk-headless \
        openjdk-8-jre openjdk-8-jre-headless default-libmysqlclient-dev \
        && rm -rf /var/lib/apt/lists/*
WORKDIR /home/user/Python-3.10.2
RUN ./configure --enable-optimizations
RUN make altinstall
CMD ["/bin/bash"]