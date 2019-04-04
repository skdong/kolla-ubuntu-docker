FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="congress-base" build-date="20190404"








RUN usermod --append --home /var/lib/congress --groups kolla congress \
    && mkdir -p /var/lib/congress \
    && chown -R 42410:42410 /var/lib/congress



    
        
    

RUN apt-get update && apt-get -y install --no-install-recommends congress-common congress-server && apt-get clean && rm -rf /var/lib/apt/lists/*



COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN touch /usr/local/bin/kolla_congress_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_congress_extend_start

