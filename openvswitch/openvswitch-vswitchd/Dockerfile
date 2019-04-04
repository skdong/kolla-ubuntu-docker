FROM kolla/ubuntu-binary-openvswitch-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="openvswitch-vswitchd" build-date="20190404"



COPY extend_start.sh /usr/local/bin/kolla_openvswitch_extend_start
RUN chmod 755 /usr/local/bin/kolla_openvswitch_extend_start


