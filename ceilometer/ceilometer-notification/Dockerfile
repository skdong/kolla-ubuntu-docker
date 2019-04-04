FROM kolla/ubuntu-binary-ceilometer-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="ceilometer-notification" build-date="20190404"






    
        
    

RUN apt-get update && apt-get -y install --no-install-recommends ceilometer-agent-notification && apt-get clean && rm -rf /var/lib/apt/lists/*



COPY extend_start.sh /usr/local/bin/kolla_ceilometer_extend_start
RUN chmod 755 /usr/local/bin/kolla_ceilometer_extend_start




USER ceilometer