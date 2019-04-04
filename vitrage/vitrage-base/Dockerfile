FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="vitrage-base" build-date="20190404"








RUN usermod --append --home /var/lib/vitrage --groups kolla vitrage \
    && mkdir -p /var/lib/vitrage \
    && chown -R 42459:42459 /var/lib/vitrage




    

RUN echo 'binary not yet available for ubuntu' \
    && /bin/false

    



COPY extend_start.sh /usr/local/bin/kolla_extend_start
RUN touch /usr/local/bin/kolla_vitrage_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_vitrage_extend_start

