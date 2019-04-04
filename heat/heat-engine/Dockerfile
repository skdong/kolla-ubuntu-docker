FROM kolla/ubuntu-binary-heat-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="heat-engine" build-date="20190404"






    
        
    
RUN apt-get update && apt-get -y install --no-install-recommends heat-engine && apt-get clean && rm -rf /var/lib/apt/lists/*





USER heat