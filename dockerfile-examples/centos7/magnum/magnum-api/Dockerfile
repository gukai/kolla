FROM kolla/centos-binary-magnum-base:1.1.3
MAINTAINER Kolla Project (https://launchpad.net/kolla)


    

RUN yum -y install openstack-magnum-api \
    && yum clean all

    


COPY extend_start.sh /usr/local/bin/kolla_magnum_extend_start
RUN chmod 755 /usr/local/bin/kolla_magnum_extend_start



USER magnum