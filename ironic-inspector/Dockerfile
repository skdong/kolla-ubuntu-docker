FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="ironic-inspector" build-date="20190404"








RUN usermod --append --home /var/lib/ironic-inspector --groups kolla ironic-inspector \
    && mkdir -p /var/lib/ironic-inspector \
    && chown -R 42461:42461 /var/lib/ironic-inspector



    
        
    

RUN apt-get update && apt-get -y install --no-install-recommends iptables ironic-inspector && apt-get clean && rm -rf /var/lib/apt/lists/*



COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN chmod 755 /usr/local/bin/kolla_extend_start \
    && chown -R ironic-inspector: /etc/ironic-inspector




USER ironic-inspector