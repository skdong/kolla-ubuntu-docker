FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="collectd" build-date="20190404"








RUN usermod --append --home /var/lib/collectd --groups kolla collectd \
    && mkdir -p /var/lib/collectd \
    && chown -R 42409:42409 /var/lib/collectd






RUN apt-get update && apt-get -y install --no-install-recommends collectd && apt-get clean && rm -rf /var/lib/apt/lists/*

COPY extend_start.sh /usr/local/bin/kolla_extend_start
RUN chmod 755 /usr/local/bin/kolla_extend_start \
    && chown -R collectd /var/lib/collectd \
    && chown -R collectd /etc/collectd* \
    && chown -R collectd /var/run/




USER collectd