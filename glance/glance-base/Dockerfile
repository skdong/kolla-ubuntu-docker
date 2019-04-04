FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="glance-base" build-date="20190404"








RUN usermod --append --home /var/lib/glance --groups kolla glance \
    && mkdir -p /var/lib/glance \
    && chown -R 42415:42415 /var/lib/glance



    
        
    

RUN apt-get update && apt-get -y install --no-install-recommends glance python-os-brick python-oslo.vmware python-rados python-rbd && apt-get clean && rm -rf /var/lib/apt/lists/*



COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN touch /usr/local/bin/kolla_glance_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_glance_extend_start

