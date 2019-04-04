FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="almanach-base" build-date="20190404"








RUN usermod --append --home /var/lib/almanach --groups kolla almanach \
    && mkdir -p /var/lib/almanach \
    && chown -R 42475:42475 /var/lib/almanach




RUN echo 'binary not yet available for ubuntu' \
    && /bin/false



COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN chmod 755 /usr/local/bin/kolla_extend_start

