FROM kolla/centos-binary-cinder-base:1.1.3
MAINTAINER Kolla Project (https://launchpad.net/kolla)


    

RUN yum install -y python-keystone \
  && yum clean all

    


COPY extend_start.sh /usr/local/bin/kolla_cinder_extend_start
RUN chmod 755 /usr/local/bin/kolla_cinder_extend_start



USER cinder