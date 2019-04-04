FROM kolla/ubuntu-binary-watcher-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="watcher-api" build-date="20190404"






    
        
    
RUN apt-get update && apt-get -y install --no-install-recommends watcher-api && apt-get clean && rm -rf /var/lib/apt/lists/*


COPY extend_start.sh /usr/local/bin/kolla_watcher_extend_start
RUN chmod 755 /usr/local/bin/kolla_watcher_extend_start




USER watcher