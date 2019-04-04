FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="bifrost-base" build-date="20190404"








RUN usermod --append --home /var/lib/bifrost --groups kolla bifrost \
    && mkdir -p /var/lib/bifrost \
    && chown -R 42404:42404 /var/lib/bifrost




RUN echo 'binary not yet available for ubuntu' && /bin/false



COPY bifrost_sudoers /etc/sudoers.d/kolla_bifrost_sudoers

RUN chmod 750 /etc/sudoers.d \
    && chmod 440 /etc/sudoers.d/kolla_bifrost_sudoers \
    && chown -R bifrost:bifrost /bifrost

