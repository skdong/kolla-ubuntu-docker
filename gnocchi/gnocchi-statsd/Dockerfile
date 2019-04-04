FROM kolla/ubuntu-binary-gnocchi-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="gnocchi-statsd" build-date="20190404"






    
RUN apt-get update && apt-get -y install --no-install-recommends gnocchi-statsd && apt-get clean && rm -rf /var/lib/apt/lists/*





USER gnocchi