FROM dcksv-linux-repo.kronshtadt.ru:5000/sogimi-astralinux-1.6:v1
LABEL Сборка Astra Linux для Быданова Артёма
COPY ./files/ ./etc/apt/
#COPY ./files/sources.list /etc/apt/
RUN apt-get update && apt-get install -y \
        qt5-default squashfs-tools python \
        cmake zip tar git subversion smbclient curl \
        java-common default-jre openjdk-8-jdk openjdk-8-jdk-headless \
        openjdk-8-jre openjdk-8-jre-headless default-libmysqlclient-dev \
        && rm -rf /var/lib/apt/lists/*
CMD ["/bin/bash"]