FROM kolla/centos-binary-base:1.1.3
MAINTAINER Kolla Project (https://launchpad.net/kolla)



RUN yum -y install haproxy \
    && yum clean all



COPY ensure_latest_config.sh /usr/local/bin/kolla_ensure_haproxy_latest_config
COPY extend_start.sh /usr/local/bin/kolla_extend_start
RUN chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_ensure_haproxy_latest_config

