FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="karbor-base" build-date="20190404"








RUN usermod --append --home /var/lib/karbor --groups kolla karbor \
    && mkdir -p /var/lib/karbor \
    && chown -R 42458:42458 /var/lib/karbor




RUN echo 'binary not yet available for ubuntu' \
    && /bin/false



COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN touch /usr/local/bin/kolla_karbor_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_karbor_extend_start

