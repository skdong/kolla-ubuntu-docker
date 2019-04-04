FROM kolla/ubuntu-binary-designate-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="designate-pool-manager" build-date="20190404"





# The bind9 package here is only to provide the rndc binary.

    
       
    

RUN apt-get update && apt-get -y install --no-install-recommends bind9 designate-pool-manager && apt-get clean && rm -rf /var/lib/apt/lists/*




USER designate