FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="tacker-base" build-date="20190404"








RUN usermod --append --home /var/lib/tacker --groups kolla tacker \
    && mkdir -p /var/lib/tacker \
    && chown -R 42446:42446 /var/lib/tacker




    

RUN echo 'binary not yet available for ubuntu' \
    && /bin/false

    





COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN touch /usr/local/bin/kolla_tacker_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_tacker_extend_start

