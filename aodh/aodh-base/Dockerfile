FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="aodh-base" build-date="20190404"








RUN usermod --append --home /var/lib/aodh --groups kolla aodh \
    && mkdir -p /var/lib/aodh \
    && chown -R 42402:42402 /var/lib/aodh



    

       

RUN apt-get update && apt-get -y install --no-install-recommends aodh-common apache2 libapache2-mod-wsgi-py3 python3-aodh python3-ldappool && apt-get clean && rm -rf /var/lib/apt/lists/*
RUN mkdir -p /var/www/cgi-bin/aodh \
    && cp -a /usr/lib/python3/dist-packages/aodh/api/app.wsgi /var/www/cgi-bin/aodh/ \
    && echo > /etc/apache2/ports.conf
    



COPY extend_start.sh /usr/local/bin/kolla_extend_start
COPY aodh_sudoers /etc/sudoers.d/kolla_aodh_sudoers

RUN chmod 750 /etc/sudoers.d \
    && chmod 640 /etc/sudoers.d/kolla_aodh_sudoers \
    && chmod 755 /var/www/cgi-bin/aodh \
    && touch /usr/local/bin/kolla_aodh_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_aodh_extend_start

