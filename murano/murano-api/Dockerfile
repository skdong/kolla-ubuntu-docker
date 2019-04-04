FROM kolla/ubuntu-binary-murano-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="murano-api" build-date="20190404"






    
RUN ln -s /usr/share/murano-common/io.murano.zip /io.murano.zip \
    && ln -s /var/cache/murano/meta/io.murano.applications.zip /io.murano.applications.zip
        
    

RUN apt-get update && apt-get -y install --no-install-recommends murano-api && apt-get clean && rm -rf /var/lib/apt/lists/*



COPY extend_start.sh /usr/local/bin/kolla_murano_extend_start
RUN chmod 755 /usr/local/bin/kolla_murano_extend_start




USER murano