FROM kolla/ubuntu-binary-keystone-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="keystone" build-date="20190404"





COPY keystone_bootstrap.sh /usr/local/bin/kolla_keystone_bootstrap
COPY extend_start.sh /usr/local/bin/kolla_extend_start
RUN chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_keystone_bootstrap


    # TODO: oraclelinux fails to install these packages. Should be added when this is fixed.
    
        
    
RUN apt-get update && apt-get -y install --no-install-recommends libapache2-mod-auth-gssapi python-requests-kerberos && apt-get clean && rm -rf /var/lib/apt/lists/*



