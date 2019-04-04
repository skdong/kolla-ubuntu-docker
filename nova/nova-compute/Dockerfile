FROM kolla/ubuntu-binary-nova-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="nova-compute" build-date="20190404"






    

        # ironic as workaround https://bugs.launchpad.net/packstack/+bug/1430388
        

RUN apt-get update && apt-get -y install --no-install-recommends ceph-common e2fsprogs genisoimage ironic-common multipath-tools nfs-common nova-compute openvswitch-switch open-iscsi parted python-guestfs python-ironicclient python-oslo.vmware python-rtslib-fb sysfsutils targetcli-fb && apt-get clean && rm -rf /var/lib/apt/lists/*

RUN rm -f /etc/nova/nova-compute.conf

    


COPY extend_start.sh /usr/local/bin/kolla_nova_extend_start
RUN chmod 755 /usr/local/bin/kolla_nova_extend_start \
    && rm -f /etc/machine-id




USER nova