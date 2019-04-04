FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="gnocchi-base" build-date="20190404"








RUN usermod --append --home /var/lib/gnocchi --groups kolla gnocchi \
    && mkdir -p /var/lib/gnocchi \
    && chown -R 42416:42416 /var/lib/gnocchi



    

       
        

RUN apt-get update && apt-get -y install --no-install-recommends apache2 build-essential gnocchi-common libapache2-mod-wsgi-py3 librados-dev python3-boto3 python3-dev python3-ldappool python3-pip python3-rados python3-setuptools && apt-get clean && rm -rf /var/lib/apt/lists/*
RUN pip3 --no-cache-dir install --upgrade cradox \
    && truncate -s 0 /etc/apache2/ports.conf

    


COPY extend_start.sh /usr/local/bin/kolla_extend_start
COPY gnocchi_sudoers /etc/sudoers.d/kolla_gnocchi_sudoers

RUN chmod 750 /etc/sudoers.d \
    && chmod 640 /etc/sudoers.d/kolla_gnocchi_sudoers \
    && touch /usr/local/bin/kolla_gnocchi_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_gnocchi_extend_start

