FROM kolla/ubuntu-binary-ovn-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="ovn-northd" build-date="20190404"






    


RUN apt-get update && apt-get -y install --no-install-recommends ovn-central && apt-get clean && rm -rf /var/lib/apt/lists/*


