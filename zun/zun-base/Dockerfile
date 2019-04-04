FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="zun-base" build-date="20190404"








RUN usermod --append --home /var/lib/zun --groups kolla zun \
    && mkdir -p /var/lib/zun \
    && chown -R 42463:42463 /var/lib/zun




RUN echo 'binary not yet available for ubuntu' \
    && /bin/false



COPY zun_sudoers /etc/sudoers.d/kolla_zun_sudoers
COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN chmod 750 /etc/sudoers.d \
    && chmod 640 /etc/sudoers.d/kolla_zun_sudoers \
    && touch /usr/local/bin/kolla_zun_extend_start \
    && chmod 755 /var/www/cgi-bin/zun \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_zun_extend_start

