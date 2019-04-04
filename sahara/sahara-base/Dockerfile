FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="sahara-base" build-date="20190404"








RUN usermod --append --home /var/lib/sahara --groups kolla sahara \
    && mkdir -p /var/lib/sahara \
    && chown -R 42441:42441 /var/lib/sahara





    

RUN apt-get update && apt-get -y install --no-install-recommends sahara-common && apt-get clean && rm -rf /var/lib/apt/lists/*



COPY sahara_sudoers /etc/sudoers.d/kolla_sahara_sudoers
COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN chmod 750 /etc/sudoers.d \
    && chmod 640 /etc/sudoers.d/kolla_sahara_sudoers \
    && touch /usr/local/bin/kolla_sahara_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_sahara_extend_start

