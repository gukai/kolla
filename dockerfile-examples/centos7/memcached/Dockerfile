FROM kolla/centos-binary-base:1.1.3
MAINTAINER Kolla Project (https://launchpad.net/kolla)




RUN yum -y install memcached \
    && yum clean all \
    && usermod -a -G kolla memcached





USER memcached