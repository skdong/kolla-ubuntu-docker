FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="ec2-api" build-date="20190404"








RUN usermod --append --home /var/lib/ec2api --groups kolla ec2api \
    && mkdir -p /var/lib/ec2api \
    && chown -R 42466:42466 /var/lib/ec2api




    

RUN echo 'binary not yet available for ubuntu' \
    && /bin/false

    





COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN chmod 755 /usr/local/bin/kolla_extend_start




USER ec2api