FROM kolla/centos-binary-nova-base:1.1.3
MAINTAINER Kolla Project (https://launchpad.net/kolla)


    

RUN yum -y install \
        openstack-nova-compute \
        openvswitch \
        sysfsutils \
        ceph-common \
        genisoimage \
    && yum clean all

    


COPY extend_start.sh /usr/local/bin/kolla_nova_extend_start
RUN chmod 755 /usr/local/bin/kolla_nova_extend_start \
    && rm -f /etc/machine-id



USER nova