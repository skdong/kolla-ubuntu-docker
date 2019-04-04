FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="placement-base" build-date="20190404"








RUN usermod --append --home /var/lib/placement --groups kolla placement \
    && mkdir -p /var/lib/placement \
    && chown -R 42482:42482 /var/lib/placement



    

        
    

RUN apt-get update && apt-get -y install --no-install-recommends mariadb-client placement-common && apt-get clean && rm -rf /var/lib/apt/lists/* \
    && cp /usr/share/placement/mysql-migrate-db.sh /opt/ \
    && chmod 755 /opt/mysql-migrate-db.sh



COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN touch /usr/local/bin/kolla_placement_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_placement_extend_start

