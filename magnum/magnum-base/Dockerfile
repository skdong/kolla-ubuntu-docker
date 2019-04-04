FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="magnum-base" build-date="20190404"








RUN usermod --append --home /var/lib/magnum --groups kolla magnum \
    && mkdir -p /var/lib/magnum \
    && chown -R 42428:42428 /var/lib/magnum



    
       
    
RUN apt-get update && apt-get -y install --no-install-recommends magnum-common && apt-get clean && rm -rf /var/lib/apt/lists/*



COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN touch /usr/local/bin/kolla_magnum_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_magnum_extend_start

