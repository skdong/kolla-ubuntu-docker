FROM kolla/ubuntu-binary-nova-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="nova-novncproxy" build-date="20190404"






    

        

    



RUN apt-get update && apt-get -y install --no-install-recommends nova-novncproxy && apt-get clean && rm -rf /var/lib/apt/lists/*




USER nova