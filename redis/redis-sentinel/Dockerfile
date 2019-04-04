FROM kolla/ubuntu-binary-redis-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="redis-sentinel" build-date="20190404"






    

RUN apt-get update && apt-get -y install --no-install-recommends redis-sentinel && apt-get clean && rm -rf /var/lib/apt/lists/*




USER redis