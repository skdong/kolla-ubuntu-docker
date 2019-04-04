FROM kolla/ubuntu-binary-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="haproxy" build-date="20190404"








RUN usermod --append --home /var/lib/haproxy --groups kolla haproxy \
    && mkdir -p /var/lib/haproxy \
    && chown -R 42454:42454 /var/lib/haproxy





    
RUN apt-get update \
    && apt-get -y install --no-install-recommends haproxy \
    || sed -i '/adduser/,+1 d' /var/lib/dpkg/info/haproxy.postinst \
    && echo "configuring packages" \
    && dpkg --configure -a \
    && echo "done" \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*





RUN apt-get update && apt-get -y install --no-install-recommends haproxy && apt-get clean && rm -rf /var/lib/apt/lists/*

RUN mkdir -p /var/lib/kolla/haproxy \
    && chown -R haproxy: /var/lib /run

COPY ensure_latest_config.sh /usr/local/bin/kolla_ensure_haproxy_latest_config
RUN chmod 755 /usr/local/bin/kolla_ensure_haproxy_latest_config


