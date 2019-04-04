FROM kolla/ubuntu-binary-karbor-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="karbor-api" build-date="20190404"





RUN echo 'binary not yet available for ubuntu' \
    && /bin/false



COPY extend_start.sh /usr/local/bin/kolla_karbor_extend_start
RUN chmod 755 /usr/local/bin/kolla_karbor_extend_start




USER karbor