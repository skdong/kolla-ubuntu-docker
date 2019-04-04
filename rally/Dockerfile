FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="rally" build-date="20190404"








RUN usermod --append --home /var/lib/rally --groups kolla rally \
    && mkdir -p /var/lib/rally \
    && chown -R 42440:42440 /var/lib/rally





    

RUN apt-get update && apt-get -y install --no-install-recommends python-os-testr rally && apt-get clean && rm -rf /var/lib/apt/lists/*


COPY extend_start.sh /usr/local/bin/kolla_extend_start
RUN chmod 755 /usr/local/bin/kolla_extend_start




USER rally