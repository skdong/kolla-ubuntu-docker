FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="watcher-base" build-date="20190404"








RUN usermod --append --home /var/lib/watcher --groups kolla watcher \
    && mkdir -p /var/lib/watcher \
    && chown -R 42451:42451 /var/lib/watcher



    
        
    
RUN apt-get update && apt-get -y install --no-install-recommends watcher-common && apt-get clean && rm -rf /var/lib/apt/lists/*



COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN touch /usr/local/bin/kolla_watcher_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_watcher_extend_start

