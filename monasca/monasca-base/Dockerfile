FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="monasca-base" build-date="20190404"








RUN usermod --append --home /var/lib/monasca --groups kolla monasca \
    && mkdir -p /var/lib/monasca \
    && chown -R 42431:42431 /var/lib/monasca




RUN echo 'binary not yet available for ubuntu' \
    && /bin/false



COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN touch /usr/local/bin/kolla_monasca_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_monasca_extend_start

