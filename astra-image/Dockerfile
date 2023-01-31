FROM sogimu/astralinux:1.6
LABEL Сборка Astra Linux для Быданова Артёма
COPY ./files/ /etc/apt/
RUN apt-get update && apt-get install -y \
        qt5-default mono-dev squashfs-tools python \
        cmake zip tar git subversion smbclient curl python-pip \
        java-common default-jre openjdk-8-jdk openjdk-8-jdk-headless \
        openjdk-8-jre openjdk-8-jre-headless default-libmysqlclient-dev \
        && rm -rf /var/lib/apt/lists/*
ADD ./python/Python-3.10.2.tgz ./home/user/
#RUN cd /service/app_lib/ && tar -xzf test_app.tar.gz && rm test_app.tar.gz
WORKDIR /home/user/Python-3.10.2
RUN ./configure --enable-optimizations
RUN make altinstall
CMD ["/bin/bash"]