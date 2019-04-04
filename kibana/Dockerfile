FROM kolla/ubuntu-binary-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="kibana" build-date="20190404"








RUN usermod --append --home /var/lib/kibana --groups kolla kibana \
    && mkdir -p /var/lib/kibana \
    && chown -R 42426:42426 /var/lib/kibana



RUN apt-get update && apt-get -y install --no-install-recommends kibana && apt-get clean && rm -rf /var/lib/apt/lists/*

COPY extend_start.sh /usr/local/bin/kolla_extend_start
RUN chmod 755 /usr/local/bin/kolla_extend_start




USER kibana