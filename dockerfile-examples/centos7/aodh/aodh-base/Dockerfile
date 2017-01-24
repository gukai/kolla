FROM kolla/centos-binary-openstack-base:1.1.3
MAINTAINER Kolla Project (https://launchpad.net/kolla)


    

RUN yum -y install \
        openstack-aodh-common \
    && yum clean all

    



RUN usermod -a -G kolla aodh