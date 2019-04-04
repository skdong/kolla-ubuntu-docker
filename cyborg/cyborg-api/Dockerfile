FROM kolla/ubuntu-binary-cyborg-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="cyborg-api" build-date="20190404"






RUN echo 'binary not yet available for ubuntu'  \
    && /bin/false






RUN echo > /etc/apache2/ports.conf



COPY extend_start.sh /usr/local/bin/kolla_cyborg_extend_start
RUN chmod 755 /usr/local/bin/kolla_cyborg_extend_start


