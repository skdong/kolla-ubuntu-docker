FROM kolla/ubuntu-binary-designate-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="designate-mdns" build-date="20190404"






    
       
    
RUN apt-get update && apt-get -y install --no-install-recommends designate-mdns && apt-get clean && rm -rf /var/lib/apt/lists/*





USER designate