FROM kolla/ubuntu-binary-mistral-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="mistral-api" build-date="20190404"






    
        
RUN apt-get update && apt-get -y install --no-install-recommends apache2 libapache2-mod-wsgi mistral-api && apt-get clean && rm -rf /var/lib/apt/lists/*
RUN echo > /etc/apache2/ports.conf
    



COPY extend_start.sh /usr/local/bin/kolla_mistral_extend_start
RUN chmod 755 /usr/local/bin/kolla_mistral_extend_start




USER mistral