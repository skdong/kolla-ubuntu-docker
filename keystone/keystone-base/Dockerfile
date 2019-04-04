FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="keystone-base" build-date="20190404"








RUN usermod --append --home /var/lib/keystone --groups kolla keystone \
    && mkdir -p /var/lib/keystone \
    && chown -R 42425:42425 /var/lib/keystone



    
        

RUN apt-get update && apt-get -y install --no-install-recommends apache2 keystone libapache2-mod-auth-mellon libapache2-mod-auth-openidc libapache2-mod-wsgi-py3 python3-ldappool && apt-get clean && rm -rf /var/lib/apt/lists/*
RUN mkdir -p /var/www/cgi-bin/keystone \
    && cp -a /usr/bin/keystone-wsgi-public /var/www/cgi-bin/keystone/main \
    && cp -a /usr/bin/keystone-wsgi-admin /var/www/cgi-bin/keystone/admin \
    && echo > /etc/apache2/ports.conf \
    && rm -f /etc/apache2/sites-enabled/keystone.conf

    


RUN chown -R keystone: /var/www/cgi-bin/keystone \
    && chmod 755 /var/www/cgi-bin/keystone/*

