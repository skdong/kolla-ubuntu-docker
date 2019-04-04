FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="freezer-base" build-date="20190404"








RUN usermod --append --home /var/lib/freezer --groups kolla freezer \
    && mkdir -p /var/lib/freezer \
    && chown -R 42414:42414 /var/lib/freezer




RUN echo 'binary not yet available for ubuntu' \
    && /bin/false



COPY freezer_sudoers /etc/sudoers.d/kolla_freezer_sudoers
COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN chmod 750 /etc/sudoers.d \
    && chmod 640 /etc/sudoers.d/kolla_freezer_sudoers \
    && touch /usr/local/bin/kolla_freezer_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_freezer_extend_start

