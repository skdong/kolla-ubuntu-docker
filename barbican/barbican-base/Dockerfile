FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="barbican-base" build-date="20190404"








RUN usermod --append --home /var/lib/barbican --groups kolla barbican \
    && usermod --append --groups nfast barbican \
    && mkdir -p /var/lib/barbican \
    && chown -R 42403:42403 /var/lib/barbican



    
        
    

RUN apt-get update && apt-get -y install --no-install-recommends barbican-common && apt-get clean && rm -rf /var/lib/apt/lists/*



COPY barbican_sudoers /etc/sudoers.d/kolla_barbican_sudoers
COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN chmod 750 /etc/sudoers.d \
    && chmod 640 /etc/sudoers.d/kolla_barbican_sudoers \
    && touch /usr/local/bin/kolla_barbican_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_barbican_extend_start

