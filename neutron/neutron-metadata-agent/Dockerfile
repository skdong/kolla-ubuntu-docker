FROM kolla/ubuntu-binary-neutron-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="neutron-metadata-agent" build-date="20190404"






    

        

    


RUN apt-get update && apt-get -y install --no-install-recommends neutron-metadata-agent && apt-get clean && rm -rf /var/lib/apt/lists/*




USER neutron