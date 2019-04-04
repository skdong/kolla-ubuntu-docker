FROM kolla/ubuntu-binary-designate-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="designate-central" build-date="20190404"






    
       
    
RUN apt-get update && apt-get -y install --no-install-recommends designate-central && apt-get clean && rm -rf /var/lib/apt/lists/*


COPY extend_start.sh /usr/local/bin/kolla_designate_extend_start
RUN chmod 755 /usr/local/bin/kolla_designate_extend_start




USER designate