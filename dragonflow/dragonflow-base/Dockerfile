FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="dragonflow-base" build-date="20190404"








RUN usermod --append --home /var/lib/dragonflow --groups kolla dragonflow \
    && mkdir -p /var/lib/dragonflow \
    && chown -R 42464:42464 /var/lib/dragonflow




RUN echo 'binary not yet available for ubuntu' \
    && /bin/false



COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN touch /usr/local/bin/kolla_dragonflow_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_dragonflow_extend_start

