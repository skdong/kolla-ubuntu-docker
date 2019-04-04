FROM kolla/ubuntu-binary-ironic-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="ironic-pxe" build-date="20190404"






    

    
        
    

RUN apt-get update && apt-get -y install --no-install-recommends apache2 ipxe libapache2-mod-wsgi pxelinux syslinux-common tftpd-hpa syslinux && apt-get clean && rm -rf /var/lib/apt/lists/*
RUN echo > /etc/apache2/ports.conf


COPY tftp-map-file /map-file
COPY extend_start.sh /usr/local/bin/kolla_ironic_extend_start
RUN chmod 755 /usr/local/bin/kolla_ironic_extend_start


