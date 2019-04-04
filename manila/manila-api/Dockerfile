FROM kolla/ubuntu-binary-manila-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="manila-api" build-date="20190404"






    
        
RUN apt-get update && apt-get -y install --no-install-recommends apache2 libapache2-mod-wsgi manila-api && apt-get clean && rm -rf /var/lib/apt/lists/*
RUN mkdir -p /var/www/cgi-bin/manila \
    && cp -a /usr/bin/manila-wsgi /var/www/cgi-bin/manila/manila-wsgi \
    && echo > /etc/apache2/ports.conf
    




COPY extend_start.sh /usr/local/bin/kolla_manila_extend_start
RUN chmod 755 /usr/local/bin/kolla_manila_extend_start \
    && chown -R manila: /var/www/cgi-bin/manila \
    && chmod 755 /var/www/cgi-bin/manila/manila-wsgi




USER manila