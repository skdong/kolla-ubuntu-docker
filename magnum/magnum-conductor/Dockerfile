FROM kolla/ubuntu-binary-magnum-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="magnum-conductor" build-date="20190404"






    
        

    
RUN apt-get update && apt-get -y install --no-install-recommends magnum-conductor && apt-get clean && rm -rf /var/lib/apt/lists/*


    # TODO(mandre) check for file integrity instead of downloading from an HTTPS source
    RUN curl -o /usr/bin/kubectl https://storage.googleapis.com/kubernetes-release/release/v1.5.4/bin/linux/amd64/kubectl \
        && chmod 755 /usr/bin/kubectl






USER magnum