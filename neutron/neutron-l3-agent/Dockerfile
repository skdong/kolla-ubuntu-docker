FROM kolla/ubuntu-binary-neutron-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="neutron-l3-agent" build-date="20190404"






   

        

   

RUN apt-get update && apt-get -y install --no-install-recommends neutron-l3-agent strongswan && apt-get clean && rm -rf /var/lib/apt/lists/*






USER neutron