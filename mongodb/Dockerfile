FROM kolla/ubuntu-binary-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="mongodb" build-date="20190404"








RUN usermod --append --home /var/lib/mongodb --groups kolla mongodb \
    && mkdir -p /var/lib/mongodb \
    && chown -R 42432:65534 /var/lib/mongodb



    




RUN apt-get update && apt-get -y install --no-install-recommends mongodb-server && apt-get clean && rm -rf /var/lib/apt/lists/*

COPY mongodb_sudoers /etc/sudoers.d/kolla_mongodb_sudoers
COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN chmod 755 /usr/local/bin/kolla_extend_start \
    && chmod 750 /etc/sudoers.d \
    && chmod 440 /etc/sudoers.d/kolla_mongodb_sudoers




USER mongodb