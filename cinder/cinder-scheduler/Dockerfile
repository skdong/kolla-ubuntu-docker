FROM kolla/ubuntu-binary-cinder-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="cinder-scheduler" build-date="20190404"






    
        

RUN apt-get update && apt-get -y install --no-install-recommends cinder-scheduler && apt-get clean && rm -rf /var/lib/apt/lists/*

    





USER cinder