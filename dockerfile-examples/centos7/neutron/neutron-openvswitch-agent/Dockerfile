FROM kolla/centos-binary-neutron-base:1.1.3
MAINTAINER Kolla Project (https://launchpad.net/kolla)


    

# Install required packages
RUN yum install -y \
        openstack-neutron-openvswitch \
        openvswitch \
    && yum clean all

    




USER neutron