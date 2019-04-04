FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="manila-base" build-date="20190404"








RUN usermod --append --home /var/lib/manila --groups kolla manila \
    && mkdir -p /var/lib/manila \
    && chown -R 42429:42429 /var/lib/manila



    

        

    

RUN apt-get update && apt-get -y install --no-install-recommends manila-common openvswitch-switch && apt-get clean && rm -rf /var/lib/apt/lists/*



COPY extend_start.sh /usr/local/bin/kolla_extend_start
COPY manila_sudoers /etc/sudoers.d/kolla_manila_sudoers

RUN chmod 750 /etc/sudoers.d \
    && chmod 440 /etc/sudoers.d/kolla_manila_sudoers \
    && touch /usr/local/bin/kolla_manila_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_manila_extend_start

