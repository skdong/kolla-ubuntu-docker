FROM kolla/ubuntu-binary-nova-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="nova-compute-ironic" build-date="20190404"








    

        
RUN apt-get update && apt-get -y install --no-install-recommends genisoimage nova-compute && apt-get clean && rm -rf /var/lib/apt/lists/*

RUN rm /etc/nova/nova-compute.conf

    






USER nova