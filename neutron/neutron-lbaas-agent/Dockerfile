FROM kolla/ubuntu-binary-neutron-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="neutron-lbaas-agent" build-date="20190404"






RUN apt-get update && apt-get -y install --no-install-recommends haproxy && apt-get clean && rm -rf /var/lib/apt/lists/*


    

        

    

RUN apt-get update && apt-get -y install --no-install-recommends neutron-lbaas-common neutron-lbaasv2-agent python3-neutron-lbaas && apt-get clean && rm -rf /var/lib/apt/lists/*



COPY extend_start.sh /usr/local/bin/kolla_neutron_extend_start
RUN chmod 755 /usr/local/bin/kolla_neutron_extend_start




USER neutron