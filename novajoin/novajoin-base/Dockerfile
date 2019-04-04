FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="novajoin-base" build-date="20190404"








RUN usermod --append --home /var/lib/novajoin --groups kolla novajoin \
    && mkdir -p /var/lib/novajoin \
    && chown -R 42470:42470 /var/lib/novajoin



    
RUN echo 'binary not yet available for ubuntu' \
    && /bin/false
    





COPY extend_start.sh /usr/local/bin/kolla_extend_start
RUN chmod 750 /etc/sudoers.d \
    && touch /usr/local/bin/kolla_novajoin_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_novajoin_extend_start

