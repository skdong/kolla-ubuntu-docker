FROM kolla/ubuntu-binary-zun-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="zun-compute" build-date="20190404"





RUN echo 'binary not yet available for ubuntu' \
    && /bin/false



COPY zun_sudoers /etc/sudoers.d/kolla_zun_sudoers
COPY extend_start.sh /usr/local/bin/kolla_zun_extend_start

RUN chmod 755 /usr/local/bin/kolla_zun_extend_start \
    && chmod 750 /etc/sudoers.d \
    && chmod 640 /etc/sudoers.d/kolla_zun_sudoers




USER zun