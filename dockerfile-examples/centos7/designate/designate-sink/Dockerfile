FROM kolla/centos-binary-designate-base:1.1.3
MAINTAINER Kolla Project (https://launchpad.net/kolla)


    

RUN yum install -y \
        openstack-designate-sink \
        python-designateclient \
    && yum clean all

    




USER designate