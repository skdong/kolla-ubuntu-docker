FROM kolla/ubuntu-binary-ironic-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="ironic-conductor" build-date="20190404"






    
        # TODO(jeffrey4l): no python-dracclient, python-oneviewclient, UcsSdk,
        # ImcSdk package, python-sushy, ironic-staging-drivers
        
    


RUN apt-get update && apt-get -y install --no-install-recommends ansible bsdmainutils dosfstools e2fsprogs gdisk ipmitool ironic-conductor parted psmisc python-ironic-inspector-client python3-proliantutils python-pysnmp4 python3-scciclient python-systemd qemu-utils shellinabox xfsprogs && apt-get clean && rm -rf /var/lib/apt/lists/*




USER ironic