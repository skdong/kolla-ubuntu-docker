FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="kuryr-base" build-date="20190404"








RUN usermod --append --home /var/lib/kuryr --groups kolla kuryr \
    && mkdir -p /var/lib/kuryr \
    && chown -R 42469:42469 /var/lib/kuryr




RUN echo 'binary not yet available for ubuntu' \
    && /bin/false



COPY extend_start.sh /usr/local/bin/kolla_extend_start
RUN chmod 755 /usr/local/bin/kolla_extend_start

