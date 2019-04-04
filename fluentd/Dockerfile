FROM kolla/ubuntu-binary-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="fluentd" build-date="20190404"






    


RUN usermod --append --home /var/lib/td-agent --groups kolla td-agent \
    && usermod --append --groups mysql td-agent \
    && mkdir -p /var/lib/td-agent \
    && chown -R 42447:42447 /var/lib/td-agent

    



RUN apt-get update && apt-get -y install --no-install-recommends g++ make ruby ruby-dev td-agent && apt-get clean && rm -rf /var/lib/apt/lists/*

# Distro specific files and operations

COPY fluentd_sudoers /etc/sudoers.d/kolla_fluentd_sudoers
RUN chmod 440 /etc/sudoers.d/kolla_fluentd_sudoers \
    && sed -i -e "s/USER=td-agent/USER=root/" -e "s/GROUP=td-agent/GROUP=root/" /etc/init.d/td-agent \
    && rm -f /etc/td-agent/td-agent.conf \
    && chown -R td-agent: /etc/td-agent



COPY extend_start.sh /usr/local/bin/kolla_extend_start
RUN chmod 755 /usr/local/bin/kolla_extend_start




    


RUN ulimit -n 65536 && td-agent-gem install fluent-plugin-elasticsearch fluent-plugin-grep fluent-plugin-grok-parser:2.1.4 fluent-plugin-kubernetes_metadata_filter fluent-plugin-parser fluent-plugin-rewrite-tag-filter:2.0.0 fluent-plugin-secure-forward

# Build and install Fluentd output plugin for Monasca Log API
ARG monasca_output_plugin_tag=0.0.1
ARG monasca_output_plugin_url=https://github.com/monasca/fluentd-monasca/archive/$monasca_output_plugin_tag.tar.gz
ADD $monasca_output_plugin_url /tmp/fluentd-monasca.tar.gz
RUN tar -xvf /tmp/fluentd-monasca.tar.gz -C /tmp \
    && cd /tmp/fluentd-monasca-* \
    && gem build fluentd-monasca-output.gemspec \
    && gem install fluentd-monasca-output-*.gem \
    && fluent-gem install fluentd-monasca-output-*.gem \
    && rm -rf /tmp/fluentd*







USER td-agent
