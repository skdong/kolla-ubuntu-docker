FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="designate-base" build-date="20190404"








RUN usermod --append --home /var/lib/designate --groups kolla designate \
    && mkdir -p /var/lib/designate \
    && chown -R 42411:42411 /var/lib/designate



    
       

RUN apt-get update && apt-get -y install --no-install-recommends designate-common python-tooz && apt-get clean && rm -rf /var/lib/apt/lists/*

    


COPY designate_sudoers /etc/sudoers.d/kolla_designate_sudoers
COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN chmod 750 /etc/sudoers.d \
    && chmod 640 /etc/sudoers.d/kolla_designate_sudoers \
    && touch /usr/local/bin/kolla_designate_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_designate_extend_start

