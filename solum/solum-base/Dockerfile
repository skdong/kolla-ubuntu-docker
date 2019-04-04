FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="solum-base" build-date="20190404"








RUN usermod --append --home /var/lib/solum --groups kolla solum \
    && mkdir -p /var/lib/solum \
    && chown -R 42444:42444 /var/lib/solum




RUN echo 'binary not yet available for ubuntu' \
    && /bin/false



COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN touch /usr/local/bin/kolla_solum_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_solum_extend_start

