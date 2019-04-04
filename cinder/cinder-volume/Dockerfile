FROM kolla/ubuntu-binary-cinder-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="cinder-volume" build-date="20190404"






    

RUN apt-get update && apt-get -y install --no-install-recommends nfs-common sysfsutils python-rtslib-fb targetcli-fb thin-provisioning-tools tgt && apt-get clean && rm -rf /var/lib/apt/lists/*


RUN sed -i '1 i include /var/lib/cinder/volumes/*' /etc/tgt/targets.conf





    
        

RUN apt-get update && apt-get -y install --no-install-recommends cinder-volume python-rtslib-fb targetcli-fb thin-provisioning-tools && apt-get clean && rm -rf /var/lib/apt/lists/*
    



COPY cinder_sudoers /etc/sudoers.d/kolla_cinder_volume_sudoers
COPY extend_start.sh /usr/local/bin/kolla_cinder_extend_start

RUN chmod 750 /etc/sudoers.d \
    && chmod 440 /etc/sudoers.d/kolla_cinder_volume_sudoers \
    && chmod 755 /usr/local/bin/kolla_cinder_extend_start




USER cinder