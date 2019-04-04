FROM kolla/ubuntu-binary-sahara-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="sahara-api" build-date="20190404"






    
        
    
RUN apt-get update && apt-get -y install --no-install-recommends sahara-api && apt-get clean && rm -rf /var/lib/apt/lists/*


COPY extend_start.sh /usr/local/bin/kolla_sahara_extend_start
RUN chmod 755 /usr/local/bin/kolla_sahara_extend_start




USER sahara