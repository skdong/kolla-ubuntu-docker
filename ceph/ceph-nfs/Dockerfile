FROM kolla/ubuntu-binary-ceph-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="ceph-nfs" build-date="20190404"






        



RUN apt-get update && apt-get -y install --no-install-recommends nfs-ganesha nfs-ganesha-ceph && apt-get clean && rm -rf /var/lib/apt/lists/*





USER ceph