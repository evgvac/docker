FROM sogimu/astralinux:1.6
LABEL Сборка Astra Linux для Быданова Артёма
COPY ./files/ /etc/apt/
RUN apt-get update && apt-get install -y \
#        mono-dev \
        qt5-default squashfs-tools python python3-dev gcc \
        cmake zip tar git subversion smbclient curl python-pip \
        java-common default-jre openjdk-8-jdk openjdk-8-jdk-headless \
        openjdk-8-jre openjdk-8-jre-headless default-libmysqlclient-dev \
        openssl libssl-dev libncurses5-dev libsqlite3-dev libreadline-dev libtk8.6 libpcap-dev \
        && rm -rf /var/lib/apt/lists/*
ADD ./python/Python-3.10.2.tgz /home/user/ 
ADD ./mariadb/mariadb-1.1.5.post3.tar /home/user/
ADD ./connector_c/mariadb-connector-c-3.1.5-src.tar.gz /home/user/
#RUN cd /service/app_lib/ && tar -xzf test_app.tar.gz && rm test_app.tar.gz
WORKDIR /home/user/Python-3.10.2
RUN ./configure --enable-optimizations
RUN make altinstall
#RUN /usr/local/bin/python3.10 -m pip install --upgrade pip
#RUN pip3.10 install mysqlclient 
#RUN pip3.10 install mariadb
CMD ["/bin/bash"]