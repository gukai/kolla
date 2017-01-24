FROM kolla/centos-binary-openstack-base:1.1.3
MAINTAINER Kolla Project (https://launchpad.net/kolla)


    

RUN curl -L https://trunk.rdoproject.org/centos7/current/delorean.repo -o /etc/yum.repos.d/delorean.repo \
    && yum install -y openstack-magnum-common \
    && yum clean all

    


COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN usermod -a -G kolla magnum \
    && touch /usr/local/bin/kolla_magnum_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_magnum_extend_start