FROM kolla/ubuntu-binary-cinder-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="cinder-api" build-date="20190404"






    
        
RUN apt-get update && apt-get -y install --no-install-recommends apache2 cinder-api libapache2-mod-wsgi-py3 && apt-get clean && rm -rf /var/lib/apt/lists/*
RUN mkdir -p /var/www/cgi-bin/cinder \
    && cp -a /usr/bin/cinder-wsgi /var/www/cgi-bin/cinder/cinder-wsgi \
    && echo > /etc/apache2/ports.conf
    



COPY extend_start.sh /usr/local/bin/kolla_cinder_extend_start
RUN chmod 755 /usr/local/bin/kolla_cinder_extend_start \
    && chown -R cinder: /var/www/cgi-bin/cinder \
    && chmod 755 /var/www/cgi-bin/cinder/cinder-wsgi


