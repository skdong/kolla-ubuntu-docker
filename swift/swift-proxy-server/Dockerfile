FROM kolla/ubuntu-binary-swift-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="swift-proxy-server" build-date="20190404"






    
        
    

RUN apt-get update && apt-get -y install --no-install-recommends swift-proxy python-ceilometermiddleware && apt-get clean && rm -rf /var/lib/apt/lists/*






USER swift