FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="cinder-base" build-date="20190404"








RUN usermod --append --home /var/lib/cinder --groups kolla cinder \
    && mkdir -p /var/lib/cinder \
    && chown -R 42407:42407 /var/lib/cinder



    
        
    
RUN apt-get update && apt-get -y install --no-install-recommends ceph-common cinder-common lvm2 cryptsetup python-oslo.vmware && apt-get clean && rm -rf /var/lib/apt/lists/*



COPY cinder_sudoers /etc/sudoers.d/kolla_cinder_sudoers
COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN chmod 750 /etc/sudoers.d \
    && chmod 440 /etc/sudoers.d/kolla_cinder_sudoers \
    && touch /usr/local/bin/kolla_cinder_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_cinder_extend_start

