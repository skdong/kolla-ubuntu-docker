FROM kolla/ubuntu-binary-trove-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="trove-guestagent" build-date="20190404"






    
        
    

RUN apt-get update && apt-get -y install --no-install-recommends trove-guestagent && apt-get clean && rm -rf /var/lib/apt/lists/*






USER trove