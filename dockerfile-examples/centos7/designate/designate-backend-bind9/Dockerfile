FROM kolla/centos-binary-designate-base:1.1.3
MAINTAINER Kolla Project (https://launchpad.net/kolla)


    

RUN yum install -y bind \
    && yum clean all \
    && mkdir -p /var/lib/kolla/ \
    && cp -pr /var/named /var/lib/kolla/var-named

    




USER designate