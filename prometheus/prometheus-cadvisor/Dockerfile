FROM kolla/ubuntu-binary-prometheus-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="prometheus-cadvisor" build-date="20190404"






ENV prometheus_cadvisor_version=0.32.0





RUN curl -ssL -o /opt/cadvisor https://github.com/google/cadvisor/releases/download/v${prometheus_cadvisor_version}/cadvisor && chmod 0755 /opt/cadvisor





