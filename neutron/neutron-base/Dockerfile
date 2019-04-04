FROM kolla/ubuntu-binary-openstack-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="neutron-base" build-date="20190404"








RUN usermod --append --home /var/lib/neutron --groups kolla neutron \
    && mkdir -p /var/lib/neutron \
    && chown -R 42435:42435 /var/lib/neutron





    
RUN apt-get update \
    && apt-get -y install --no-install-recommends haproxy \
    || sed -i '/adduser/,+1 d' /var/lib/dpkg/info/haproxy.postinst \
    && echo "configuring packages" \
    && dpkg --configure -a \
    && echo "done" \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*





    

        

        

             # FIXED(jeffrey4l): UCA rocky release is not include python-vmware-nsx
             # 13.0.0 package now.  add 'python-vmware-nsx' into
             # neutron_base_packages list after UCA fixed the issue.
             

        
        

    
RUN apt-get update \
    && apt-get -y install --no-install-recommends haproxy \
    || sed -i '/adduser/,+1 d' /var/lib/dpkg/info/haproxy.postinst \
    && echo "configuring packages" \
    && dpkg --configure -a \
    && echo "done" \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*


    

RUN apt-get update && apt-get -y install --no-install-recommends iproute2 iputils-ping keepalived net-tools radvd neutron-plugin-ml2 neutron-server openvswitch-switch python3-networking-sfc python-openvswitch python-oslo.vmware neutron-lbaas-common python3-neutron-fwaas && apt-get clean && rm -rf /var/lib/apt/lists/*

    

RUN mkdir -p /usr/share/neutron \
    && ln -s /etc/neutron/api-paste.ini /usr/share/neutron/api-paste.ini

    



COPY neutron_sudoers /etc/sudoers.d/kolla_neutron_sudoers
COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN chmod 750 /etc/sudoers.d \
    && chmod 440 /etc/sudoers.d/kolla_neutron_sudoers \
    && touch /usr/local/bin/kolla_neutron_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_neutron_extend_start

