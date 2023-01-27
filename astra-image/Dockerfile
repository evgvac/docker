FROM dcksv-linux-repo.kronshtadt.ru:5000/sogimi-astralinux-1.6:v1
COPY ./files  ./etc/apt/
#COPY ./files/sources.list /etc/apt/
RUN apt-get update && apt-get install mono-dev qt5-default squashfs-tools python cmake zip tar git subversion smbclient curl java-common default-jre openjdk-8-jdk openjdk-8-jdk-headless openjdk-8-jre openjdk-8-jre-headless default-libmysqlclient-dev 
#CMD echo "Hellow Astra Linux smolensk 1.6"