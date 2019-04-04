FROM kolla/ubuntu-binary-barbican-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="barbican-worker" build-date="20190404"






    
       
    

RUN apt-get update && apt-get -y install --no-install-recommends barbican-worker && apt-get clean && rm -rf /var/lib/apt/lists/*






USER barbican