FROM kolla/ubuntu-binary-congress-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="congress-api" build-date="20190404"



COPY extend_start.sh /usr/local/bin/kolla_congress_extend_start
RUN chmod 755 /usr/local/bin/kolla_congress_extend_start




USER congress