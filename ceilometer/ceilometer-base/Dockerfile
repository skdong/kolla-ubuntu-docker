FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="ceilometer-base" build-date="20190404"








RUN usermod --append --home /var/lib/ceilometer --groups kolla ceilometer \
    && mkdir -p /var/lib/ceilometer \
    && chown -R 42405:42405 /var/lib/ceilometer



    
        
    

RUN apt-get update && apt-get -y install --no-install-recommends ceilometer-common python-gnocchiclient python3-panko python-pymongo && apt-get clean && rm -rf /var/lib/apt/lists/*



COPY ceilometer_sudoers /etc/sudoers.d/kolla_ceilometer_sudoers
COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN chmod 750 /etc/sudoers.d \
    && chmod 440 /etc/sudoers.d/kolla_ceilometer_sudoers \
    && touch /usr/local/bin/kolla_ceilometer_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_ceilometer_extend_start

