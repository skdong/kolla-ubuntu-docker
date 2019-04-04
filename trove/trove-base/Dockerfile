FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="trove-base" build-date="20190404"








RUN usermod --append --home /var/lib/trove --groups kolla trove \
    && mkdir -p /var/lib/trove \
    && chown -R 42449:42449 /var/lib/trove




    
        
    

RUN apt-get update && apt-get -y install --no-install-recommends trove-common && apt-get clean && rm -rf /var/lib/apt/lists/*



COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN touch /usr/local/bin/kolla_trove_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_trove_extend_start

