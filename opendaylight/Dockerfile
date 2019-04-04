FROM kolla/ubuntu-binary-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="opendaylight" build-date="20190404"








RUN usermod --append --home /var/lib/odl --groups kolla odl \
    && mkdir -p /var/lib/odl \
    && chown -R 42462:42462 /var/lib/odl





    
    # NOTE(egonzalez): ODL fails to install in debian family images with
    # existing odl user. First install odl and then allow usage of
    # install_packages macro for custom configs.
    
        

    
RUN apt-get update \
    && apt-get -y install --no-install-recommends opendaylight \
    || sed -i '/adduser/,+1 d' /var/lib/dpkg/info/opendaylight.postinst \
    && echo "configuring packages" \
    && dpkg --configure -a \
    && echo "done" \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*


    


RUN apt-get update && apt-get -y install --no-install-recommends opendaylight openjdk-8-jre-headless && apt-get clean && rm -rf /var/lib/apt/lists/*



COPY extend_start.sh /usr/local/bin/kolla_extend_start
RUN chmod 755 /usr/local/bin/kolla_extend_start


