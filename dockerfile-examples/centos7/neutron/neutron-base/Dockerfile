FROM kolla/centos-binary-openstack-base:1.1.3
MAINTAINER Kolla Project (https://launchpad.net/kolla)


    

RUN yum -y install \
        openstack-neutron \
        openstack-neutron-ml2 \
        python-neutron \
        openvswitch \
    && yum clean all

    


COPY neutron_sudoers /etc/sudoers.d/kolla_neutron_sudoers
COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN usermod -a -G kolla neutron \
    && chmod 750 /etc/sudoers.d \
    && chmod 440 /etc/sudoers.d/kolla_neutron_sudoers \
    && touch /usr/local/bin/kolla_neutron_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_neutron_extend_start