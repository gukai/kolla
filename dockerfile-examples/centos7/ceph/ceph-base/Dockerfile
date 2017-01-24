FROM kolla/centos-binary-base:1.1.3
MAINTAINER Kolla Project (https://launchpad.net/kolla)



RUN yum -y install \
        ceph \
        ceph-radosgw \
        parted \
        hdparm \
        btrfs-progs \
    && yum clean all



COPY extend_start.sh /usr/local/bin/kolla_extend_start
RUN chmod 755 /usr/local/bin/kolla_extend_start

RUN useradd --user-group ceph \
    && mkdir -p /home/ceph \
    && chown -R ceph: /home/ceph