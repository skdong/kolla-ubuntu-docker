FROM kolla/ubuntu-binary-cinder-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="cinder-backup" build-date="20190404"






    
        
    



RUN apt-get update && apt-get -y install --no-install-recommends cinder-backup nfs-common && apt-get clean && rm -rf /var/lib/apt/lists/*




USER cinder