FROM kolla/ubuntu-binary-solum-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="solum-api" build-date="20190404"





RUN echo 'binary not yet available for ubuntu' \
    && /bin/false



COPY extend_start.sh /usr/local/bin/kolla_solum_extend_start
RUN chmod 755 /usr/local/bin/kolla_solum_extend_start




USER solum