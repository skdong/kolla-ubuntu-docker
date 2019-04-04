FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="heat-base" build-date="20190404"








RUN usermod --append --home /var/lib/heat --groups kolla heat \
    && mkdir -p /var/lib/heat \
    && chown -R 42418:42418 /var/lib/heat





    
RUN apt-get update && apt-get -y install --no-install-recommends apache2 heat-common libapache2-mod-wsgi && apt-get clean && rm -rf /var/lib/apt/lists/*
RUN echo > /etc/apache2/ports.conf




COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN touch /usr/local/bin/kolla_heat_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_heat_extend_start

