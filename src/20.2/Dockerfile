FROM oracle/graalvm-ce:20.3.0-java11

MAINTAINER eugen@cloud-surfers.de
RUN yum -y install wget yum-utils;\
    yum-config-manager \
        --add-repo \
        https://download.docker.com/linux/centos/docker-ce.repo ; \
    yum -y install  docker-ce-cli containerd.io ; \
    wget https://ftp-stud.hs-esslingen.de/pub/Mirrors/ftp.apache.org/dist/maven/maven-3/3.6.3/binaries/apache-maven-3.6.3-bin.tar.gz -O /tmp/maven.tar.gz ; \
    tar -C /opt -xvf /tmp/maven.tar.gz; mv /opt/apache-maven-3.6.3 /opt/maven-3; ln -s /opt/maven-3/bin/mvn /usr/bin/mvn ; \
    gu install native-image