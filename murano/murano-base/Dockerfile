FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="murano-base" build-date="20190404"








RUN usermod --append --home /var/lib/murano --groups kolla murano \
    && mkdir -p /var/lib/murano \
    && chown -R 42433:42433 /var/lib/murano




    
        
    

RUN apt-get update && apt-get -y install --no-install-recommends murano-common && apt-get clean && rm -rf /var/lib/apt/lists/*



COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN touch /usr/local/bin/kolla_murano_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_murano_extend_start

