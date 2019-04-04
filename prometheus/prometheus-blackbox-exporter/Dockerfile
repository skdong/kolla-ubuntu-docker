FROM kolla/ubuntu-binary-prometheus-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="prometheus-blackbox-exporter" build-date="20190404"




ENV blackbox_exporter_version=0.13.0



RUN curl -sSL -o /tmp/blackbox_exporter.tar.gz https://github.com/prometheus/blackbox_exporter/releases/download/v${blackbox_exporter_version}/blackbox_exporter-${blackbox_exporter_version}.linux-amd64.tar.gz \
    && tar xvf /tmp/blackbox_exporter.tar.gz -C /opt/ \
    && rm -f /tmp/blackbox_exporter.tar.gz \
    && ln -s /opt/blackbox_exporter* /opt/blackbox_exporter





USER prometheus