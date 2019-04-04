FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="searchlight-base" build-date="20190404"








RUN usermod --append --home /var/lib/searchlight --groups kolla searchlight \
    && mkdir -p /var/lib/searchlight \
    && chown -R 42442:42442 /var/lib/searchlight




RUN echo 'binary not yet available for ubuntu' \
    && /bin/false



COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN touch /usr/local/bin/kolla_searchlight_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_searchlight_extend_start

