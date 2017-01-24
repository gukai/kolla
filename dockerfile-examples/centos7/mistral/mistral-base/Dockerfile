FROM kolla/centos-binary-openstack-base:1.1.3
MAINTAINER Kolla Project (https://launchpad.net/kolla)



RUN echo 'binary not yet available for centos' \
    && /bin/false



COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN usermod -a -G kolla mistral \
    && touch /usr/local/bin/kolla_mistral_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_mistral_extend_start