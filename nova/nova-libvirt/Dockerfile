FROM kolla/ubuntu-binary-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="nova-libvirt" build-date="20190404"








RUN usermod --append --home /var/lib/nova --groups kolla nova \
    && usermod --append --groups qemu nova \
    && mkdir -p /var/lib/nova \
    && chown -R 42436:42436 /var/lib/nova




    

    

    
        
    

    


RUN apt-get update && apt-get -y install --no-install-recommends ceph-common ebtables libvirt-clients libvirt-daemon-system openvswitch-switch pm-utils qemu-block-extra qemu-kvm qemu-system trousers dmidecode xen-utils && apt-get clean && rm -rf /var/lib/apt/lists/*



RUN rm -f /etc/libvirt/qemu/networks/default.xml /etc/libvirt/qemu/networks/autostart/default.xml



COPY extend_start.sh /usr/local/bin/kolla_extend_start
RUN chmod 755 /usr/local/bin/kolla_extend_start


