FROM kolla/ubuntu-binary-ceilometer-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="ceilometer-compute" build-date="20190404"






    
        
    
RUN apt-get update && apt-get -y install --no-install-recommends ceilometer-agent-compute python-libvirt && apt-get clean && rm -rf /var/lib/apt/lists/*






# NOTE(huikang): non-root user does not work with libvirt.sock.
#                Need configuration in nova-libvirt container to allow
#                USER ceilometer to access libvirt.sock