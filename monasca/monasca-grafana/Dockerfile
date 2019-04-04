FROM kolla/ubuntu-binary-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="monasca-grafana" build-date="20190404"







RUN usermod --append --home /usr/share/grafana --groups kolla monasca \
    && mkdir -p /usr/share/grafana \
    && chown -R 42431:42431 /usr/share/grafana



    


RUN apt-get update && apt-get -y install --no-install-recommends golang git npm bzip2 g++ make ruby ruby-dev fontconfig rpm && apt-get clean && rm -rf /var/lib/apt/lists/*

WORKDIR /usr/share/grafana

COPY grafana_sudoers /etc/sudoers.d/kolla_grafana_sudoers
COPY extend_start.sh /usr/local/bin/kolla_extend_start

ENV GO_PATH=/grafana
ENV monasca_grafana_build_path=${GO_PATH}/src/github.com/grafana/grafana
ARG monasca_grafana_version=grafana4
ARG monasca_grafana_url=https://github.com/monasca/grafana/archive/$monasca_grafana_version.tar.gz


RUN gem install rake fpm \
    && curl -sSL -o /tmp/monasca-grafana.tgz ${monasca_grafana_url} \
    && mkdir -p ${monasca_grafana_build_path} \
    && tar --strip 1 -xvf /tmp/monasca-grafana.tgz -C ${monasca_grafana_build_path} \
    && rm -f /tmp/monasca-grafana.tgz \
    && cd ${monasca_grafana_build_path} \
    && go run build.go setup \
    && npm install \
    && go run build.go build package \
    && mv ${monasca_grafana_build_path}/dist /grafana_pkgs \
    && rm -rf /grafana


  


RUN apt-get update && apt-get -y install --no-install-recommends /grafana_pkgs/grafana*.deb && apt-get clean && rm -rf /var/lib/apt/lists/*



RUN grafana-cli plugins install monasca-datasource \
    && chmod 750 /etc/sudoers.d \
    && chmod 440 /etc/sudoers.d/kolla_grafana_sudoers \
    && chmod 755 /usr/local/bin/kolla_extend_start




USER monasca