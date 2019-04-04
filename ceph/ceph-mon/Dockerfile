FROM kolla/ubuntu-binary-ceph-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="ceph-mon" build-date="20190404"



COPY fetch_ceph_keys.py /usr/bin/

COPY extend_start.sh /usr/local/bin/kolla_extend_start
RUN chmod 755 /usr/local/bin/kolla_extend_start /usr/bin/fetch_ceph_keys.py


