FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="tempest" build-date="20190404"








RUN usermod --append --home /var/lib/tempest --groups kolla tempest \
    && mkdir -p /var/lib/tempest \
    && chown -R 42480:42480 /var/lib/tempest



    
        

RUN apt-get update && apt-get -y install --no-install-recommends tempest && apt-get clean && rm -rf /var/lib/apt/lists/*
RUN ln -sf /var/lib/tempest /tempest

    



WORKDIR /tempest

COPY extend_start.sh /usr/local/bin/kolla_extend_start
RUN chmod 755 /usr/local/bin/kolla_extend_start




USER tempest