FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="cloudkitty-base" build-date="20190404"








RUN usermod --append --home /var/lib/cloudkitty --groups kolla cloudkitty \
    && mkdir -p /var/lib/cloudkitty \
    && chown -R 42408:42408 /var/lib/cloudkitty



    

RUN echo 'binary not yet available for ubuntu' \
    && /bin/false

    





COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN touch /usr/local/bin/kolla_cloudkitty_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_cloudkitty_extend_start

