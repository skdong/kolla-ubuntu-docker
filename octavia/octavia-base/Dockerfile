FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="octavia-base" build-date="20190404"








RUN usermod --append --home /var/lib/octavia --groups kolla octavia \
    && mkdir -p /var/lib/octavia \
    && chown -R 42437:42437 /var/lib/octavia



    
RUN echo 'binary not yet available for ubuntu' \
            && /bin/false
    





COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN touch /usr/local/bin/kolla_octavia_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_octavia_extend_start

