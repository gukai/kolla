FROM kolla/centos-binary-openstack-base:1.1.3
MAINTAINER Kolla Project (https://launchpad.net/kolla)


    

RUN yum -y install openstack-zaqar \
    && yum clean all

    


COPY extend_start.sh /usr/local/bin/kolla_extend_start
RUN chmod 755 /usr/local/bin/kolla_extend_start \
    && usermod -a -G kolla zaqar



USER zaqar