FROM kolla/centos-binary-nova-base:1.1.3
MAINTAINER Kolla Project (https://launchpad.net/kolla)


    

RUN yum -y install \
        openstack-nova-network \
        bridge-utils \
        initscripts \
    && yum clean all

    




USER nova