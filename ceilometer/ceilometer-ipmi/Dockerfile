FROM kolla/ubuntu-binary-ceilometer-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="ceilometer-ipmi" build-date="20190404"






    
        
    



RUN apt-get update && apt-get -y install --no-install-recommends ceilometer-agent-ipmi && apt-get clean && rm -rf /var/lib/apt/lists/*




USER ceilometer