FROM kolla/ubuntu-binary-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="etcd" build-date="20190404"








RUN usermod --append --home /var/lib/etcd --groups kolla etcd \
    && mkdir -p /var/lib/etcd \
    && chown -R 42413:42413 /var/lib/etcd



    

RUN apt-get update && apt-get -y install --no-install-recommends etcd && apt-get clean && rm -rf /var/lib/apt/lists/*

COPY etcd_sudoers /etc/sudoers.d/kolla_etcd_sudoers
COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN chmod 755 /usr/local/bin/kolla_extend_start \
    && chmod 750 /etc/sudoers.d \
    && chmod 440 /etc/sudoers.d/kolla_etcd_sudoers




USER etcd