FROM kolla/centos-binary-designate-base:1.1.3
MAINTAINER Kolla Project (https://launchpad.net/kolla)


    

RUN yum install -y \
        openstack-designate-api \
    && yum clean all

    


COPY extend_start.sh /usr/local/bin/kolla_extend_start
RUN chmod 755 /usr/local/bin/kolla_extend_start



USER designate