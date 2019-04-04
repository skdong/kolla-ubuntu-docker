FROM kolla/ubuntu-binary-mistral-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="mistral-executor" build-date="20190404"






    
        
    
RUN apt-get update && apt-get -y install --no-install-recommends mistral-executor && apt-get clean && rm -rf /var/lib/apt/lists/*





USER mistral