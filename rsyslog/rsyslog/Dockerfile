FROM kolla/ubuntu-binary-rsyslog-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="rsyslog" build-date="20190404"






    


RUN apt-get update && apt-get -y install --no-install-recommends rsyslog-gnutls && apt-get clean && rm -rf /var/lib/apt/lists/*


