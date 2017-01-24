FROM kolla/centos-binary-designate-base:1.1.3
MAINTAINER Kolla Project (https://launchpad.net/kolla)


    

# The bind9 package here is only to provide the rndc binary.
RUN yum install -y \
        openstack-designate-pool-manager \
        bind \
    && yum clean all

    




USER designate