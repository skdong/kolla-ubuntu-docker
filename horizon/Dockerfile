FROM kolla/ubuntu-binary-openstack-base:rocky
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="horizon" build-date="20190404"








RUN usermod --append --home /var/lib/horizon --groups kolla horizon \
    && mkdir -p /var/lib/horizon \
    && chown -R 42420:42420 /var/lib/horizon



    
        
	#NOTE(hrw): check for python-murano-dashboard python-neutron-lbaas-dashboard
RUN apt-get update && apt-get -y install --no-install-recommends apache2 gettext libapache2-mod-wsgi locales openstack-dashboard python-designate-dashboard python-manila-ui python-murano-dashboard python-sahara-dashboard python-trove-dashboard tzdata && apt-get clean && rm -rf /var/lib/apt/lists/*



RUN echo > /etc/apache2/ports.conf \
    && sed -i 's|\(ServerTokens \)OS|\1Prod|' /etc/apache2/conf-available/security.conf \
    && ln -s ../mods-available/headers.load  /etc/apache2/mods-enabled/headers.load \
    && ln -s ../mods-available/expires.load  /etc/apache2/mods-enabled/expires.load \
    && cp /usr/share/openstack-dashboard/openstack_dashboard/conf/*.json /etc/openstack-dashboard \
    && cp /usr/share/openstack-dashboard/manage.py /usr/bin/manage.py \
    && rm /etc/apache2/conf-enabled/openstack-dashboard.conf \
    && rm /etc/openstack-dashboard/local_settings.py \
    && rm /usr/share/openstack-dashboard/openstack_dashboard/local/local_settings.py \
    && ln -s /etc/openstack-dashboard/local_settings /usr/share/openstack-dashboard/openstack_dashboard/local/local_settings.py \
    && ln -s /usr/share/openstack-dashboard/openstack_dashboard /usr/lib/python2.7/site-packages/openstack_dashboard \
    && ln -s /usr/share/openstack-dashboard/static /usr/lib/python2.7/site-packages/static \
    && for locale in /usr/lib/python2.7/site-packages/*/locale; do \
           (cd ${locale%/*} && /usr/bin/python /usr/bin/manage.py compilemessages) \
       done


    


COPY extend_start.sh /usr/local/bin/kolla_extend_start
RUN chmod 755 /usr/local/bin/kolla_extend_start


