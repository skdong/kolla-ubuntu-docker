FROM kolla/ubuntu-binary-neutron-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="neutron-server" build-date="20190404"






    

        

    

RUN apt-get update && apt-get -y install --no-install-recommends neutron-lbaasv2-agent python3-neutron-dynamic-routing python3-neutron-lbaas python3-neutron-vpnaas && apt-get clean && rm -rf /var/lib/apt/lists/*



COPY extend_start.sh /usr/local/bin/kolla_neutron_extend_start
RUN chmod 755 /usr/local/bin/kolla_neutron_extend_start




USER neutron