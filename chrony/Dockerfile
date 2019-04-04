FROM kolla/ubuntu-binary-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="chrony" build-date="20190404"








RUN usermod --append --home /var/lib/chrony --groups kolla chrony \
    && mkdir -p /var/lib/chrony \
    && chown -R 42406:42406 /var/lib/chrony




RUN apt-get update && apt-get -y install --no-install-recommends chrony && apt-get clean && rm -rf /var/lib/apt/lists/*

COPY extend_start.sh /usr/local/bin/kolla_extend_start
RUN chmod 755 /usr/local/bin/kolla_extend_start


