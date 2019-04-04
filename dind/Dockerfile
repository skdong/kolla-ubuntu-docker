FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="dind" build-date="20190404"






    

    
        
    

    
        
    
RUN apt-get update && apt-get -y install --no-install-recommends btrfs-progs openssh-server docker.io python-setuptools && apt-get clean && rm -rf /var/lib/apt/lists/*



RUN pip --no-cache-dir install --upgrade docker



COPY start.sh /usr/local/bin/kolla_start
RUN chmod 755 /usr/local/bin/kolla_start


