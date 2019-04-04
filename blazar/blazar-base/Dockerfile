FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="blazar-base" build-date="20190404"








RUN usermod --append --home /var/lib/blazar --groups kolla blazar \
    && mkdir -p /var/lib/blazar \
    && chown -R 42471:42471 /var/lib/blazar




RUN echo 'binary not yet available for ubuntu' \
    && /bin/false



COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN touch /usr/local/bin/kolla_blazar_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_blazar_extend_start

