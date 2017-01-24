FROM kolla/centos-binary-mesos-base:1.1.3
MAINTAINER Kolla Project (https://launchpad.net/kolla)



RUN yum install -y \
        marathon \
    && yum clean all



RUN useradd --user-group marathon \
    && chmod 755 /usr/bin/marathon

CMD ["marathon", "--no-logger"]



USER marathon