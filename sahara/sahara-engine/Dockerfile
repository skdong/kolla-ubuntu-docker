FROM kolla/ubuntu-binary-sahara-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="sahara-engine" build-date="20190404"






    
        
    


RUN apt-get update && apt-get -y install --no-install-recommends netcat sahara-engine && apt-get clean && rm -rf /var/lib/apt/lists/*




USER sahara