FROM kolla/ubuntu-binary-neutron-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="neutron-linuxbridge-agent" build-date="20190404"






    

        

    



RUN apt-get update && apt-get -y install --no-install-recommends ebtables neutron-linuxbridge-agent && apt-get clean && rm -rf /var/lib/apt/lists/*




USER neutron