FROM kolla/centos-binary-base:1.1.3
MAINTAINER Kolla Project (https://launchpad.net/kolla)

RUN useradd -r -m --user-group kibana \
    && usermod -a -G kolla kibana



RUN yum -y install \
        kibana \
    && yum clean all





USER kibana