FROM kolla/ubuntu-binary-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="ovsdpdk" build-date="20190404"










RUN apt-get update && apt-get -y install --no-install-recommends openvswitch-switch-dpdk && apt-get clean && rm -rf /var/lib/apt/lists/*

RUN update-alternatives --set ovs-vswitchd /usr/lib/openvswitch-switch-dpdk/ovs-vswitchd-dpdk





COPY extend_start.sh /usr/local/bin/kolla_extend_start
RUN chmod 755 /usr/local/bin/kolla_extend_start


