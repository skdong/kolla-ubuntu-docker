FROM kolla/ubuntu-binary-neutron-server:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="neutron-server-opendaylight" build-date="20190404"

USER root






    
        
    

RUN apt-get update && apt-get -y install --no-install-recommends python3-networking-bgpvpn python3-networking-l2gw python3-networking-odl && apt-get clean && rm -rf /var/lib/apt/lists/*






USER neutron