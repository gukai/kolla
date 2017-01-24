FROM kolla/centos-binary-mesos-base:1.1.3
MAINTAINER Kolla Project (https://launchpad.net/kolla)



RUN yum install -y \
        chronos \
    && yum clean all



RUN useradd --user-group chronos

CMD chronos run_jar --http_port $CHRONOS_HTTP_PORT --master $CHRONOS_MASTER --zk_hosts $CHRONOS_ZK_HOSTS



USER chronos