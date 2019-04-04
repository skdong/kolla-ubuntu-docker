FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="zaqar-base" build-date="20190404"








RUN usermod --append --home /var/lib/zaqar --groups kolla zaqar \
    && mkdir -p /var/lib/zaqar \
    && chown -R 42452:42452 /var/lib/zaqar




    
        

RUN apt-get update && apt-get -y install --no-install-recommends zaqar-common apache2 libapache2-mod-wsgi python3-ldappool && apt-get clean && rm -rf /var/lib/apt/lists/* \
    && mkdir -p /var/www/cgi-bin/zaqar \
    && chown -R zaqar: /var/www/cgi-bin/zaqar \
    && cp -a /usr/lib/python3/dist-packages/zaqar/transport/wsgi/app.py /var/www/cgi-bin/zaqar/ \
    && echo > /etc/apache2/ports.conf
    



COPY extend_start.sh /usr/local/bin/kolla_extend_start
RUN touch /usr/local/bin/kolla_zaqar_extend_start \
    && chmod 755 /var/www/cgi-bin/zaqar \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_zaqar_extend_start

