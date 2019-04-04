FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="mistral-base" build-date="20190404"








RUN usermod --append --home /var/lib/mistral --groups kolla mistral \
    && mkdir -p /var/lib/mistral \
    && chown -R 42430:42430 /var/lib/mistral




    
        
    
RUN apt-get update && apt-get -y install --no-install-recommends mistral-common redis-server && apt-get clean && rm -rf /var/lib/apt/lists/*



COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN touch /usr/local/bin/kolla_mistral_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_mistral_extend_start

