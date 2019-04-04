FROM kolla/ubuntu-binary-ceph-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="cephfs-fuse" build-date="20190404"






# Clear any customisation by Kolla to entrypoint & command
ENTRYPOINT ["/usr/bin/ceph-fuse"]
CMD []