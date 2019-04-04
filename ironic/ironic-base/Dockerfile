FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="ironic-base" build-date="20190404"








RUN usermod --append --home /var/lib/ironic --groups kolla ironic \
    && mkdir -p /var/lib/ironic \
    && chown -R 42422:42422 /var/lib/ironic



    
        
    

RUN apt-get update && apt-get -y install --no-install-recommends ironic-common && apt-get clean && rm -rf /var/lib/apt/lists/*



COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN touch /usr/local/bin/kolla_ironic_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_ironic_extend_start \
    && chown -R ironic: /etc/ironic

