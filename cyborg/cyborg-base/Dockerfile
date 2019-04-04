FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="cyborg-base" build-date="20190404"








RUN usermod --append --home /var/lib/cyborg --groups kolla cyborg \
    && mkdir -p /var/lib/cyborg \
    && chown -R 42483:42483 /var/lib/cyborg




RUN echo 'binary not yet available for ubuntu' \
    && /bin/false



COPY extend_start.sh /usr/local/bin/kolla_extend_start
COPY cyborg_sudoers /etc/sudoers.d/kolla_cyborg_sudoers

RUN chmod 750 /etc/sudoers.d \
    && touch /usr/local/bin/kolla_cyborg_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_cyborg_extend_start


