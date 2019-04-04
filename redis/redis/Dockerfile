FROM kolla/ubuntu-binary-redis-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="redis" build-date="20190404"






    

RUN apt-get update && apt-get -y install --no-install-recommends redis-server && apt-get clean && rm -rf /var/lib/apt/lists/*




USER redis