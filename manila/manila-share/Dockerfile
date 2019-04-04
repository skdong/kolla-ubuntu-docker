FROM kolla/ubuntu-binary-manila-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="manila-share" build-date="20190404"






    
        

    

RUN apt-get update && apt-get -y install --no-install-recommends manila-share ceph-common && apt-get clean && rm -rf /var/lib/apt/lists/*






USER manila