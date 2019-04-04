FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="vmtp" build-date="20190404"








RUN usermod --append --home /var/lib/vmtp --groups kolla vmtp \
    && mkdir -p /var/lib/vmtp \
    && chown -R 42450:42450 /var/lib/vmtp




RUN echo 'binary not yet available for ubuntu' \
    && /bin/false



COPY vmtp_sudoers /etc/sudoers.d/kolla_vmtp_sudoers
RUN chmod 750 /etc/sudoers.d \
    && chmod 440 /etc/sudoers.d/kolla_vmtp_sudoers




USER vmtp