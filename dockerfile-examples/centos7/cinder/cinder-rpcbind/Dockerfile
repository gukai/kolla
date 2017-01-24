FROM kolla/centos-binary-cinder-base:1.1.3
MAINTAINER Kolla Project (https://launchpad.net/kolla)



RUN yum -y install \
        nfs-utils \
        nfs-utils-lib \
    && yum clean all





USER cinder