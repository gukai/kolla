FROM kolla/centos-binary-mesosphere-base:1.1.3
MAINTAINER Kolla Project (https://launchpad.net/kolla)



RUN yum install -y \
        mesosphere-zookeeper \
    && yum clean all

RUN useradd --user-group zookeeper



COPY zookeeper_sudoers /etc/sudoers.d/zookeeper_sudoers
COPY extend_start.sh /usr/local/bin/kolla_extend_start
RUN chmod 755 /usr/local/bin/kolla_extend_start \
    && chmod 750 /etc/sudoers.d \
    && chmod 440 /etc/sudoers.d/zookeeper_sudoers \
    && usermod -a -G kolla zookeeper

ENV ZOOCFGDIR=/etc/zookeeper/conf



USER zookeeper