FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="senlin-base" build-date="20190404"








RUN usermod --append --home /var/lib/senlin --groups kolla senlin \
    && mkdir -p /var/lib/senlin \
    && chown -R 42443:42443 /var/lib/senlin



    
        
    

RUN apt-get update && apt-get -y install --no-install-recommends senlin-common && apt-get clean && rm -rf /var/lib/apt/lists/*



COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN touch /usr/local/bin/kolla_senlin_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_senlin_extend_start

