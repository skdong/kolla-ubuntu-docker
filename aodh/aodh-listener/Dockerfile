FROM kolla/ubuntu-binary-aodh-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="aodh-listener" build-date="20190404"






    
        
    
RUN apt-get update && apt-get -y install --no-install-recommends aodh-listener && apt-get clean && rm -rf /var/lib/apt/lists/*





USER aodh