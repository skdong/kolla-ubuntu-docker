FROM kolla/ubuntu-binary-watcher-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="watcher-engine" build-date="20190404"






    
        
    
RUN apt-get update && apt-get -y install --no-install-recommends watcher-decision-engine && apt-get clean && rm -rf /var/lib/apt/lists/*





USER watcher