FROM kolla/ubuntu-binary-nova-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="nova-placement-api" build-date="20190404"






    

        

RUN apt-get update && apt-get -y install --no-install-recommends apache2 libapache2-mod-wsgi-py3 nova-placement-api && apt-get clean && rm -rf /var/lib/apt/lists/*
RUN truncate -s 0 /etc/apache2/ports.conf

    


COPY extend_start.sh /usr/local/bin/kolla_nova_extend_start
RUN chmod 755 /usr/local/bin/kolla_nova_extend_start


