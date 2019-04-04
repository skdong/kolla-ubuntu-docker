FROM kolla/ubuntu-binary-barbican-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="barbican-api" build-date="20190404"






    
        

RUN apt-get update && apt-get -y install --no-install-recommends apache2 barbican-api libapache2-mod-wsgi-py3 uwsgi-plugin-python && apt-get clean && rm -rf /var/lib/apt/lists/*

RUN echo > /etc/apache2/ports.conf

    



COPY extend_start.sh /usr/local/bin/kolla_barbican_extend_start

RUN chmod 755 /usr/local/bin/kolla_barbican_extend_start




USER barbican