FROM kolla/ubuntu-binary-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="logstash" build-date="20190404"







RUN usermod --append --home /usr/share/logstash --groups kolla logstash \
    && chsh --shell /bin/bash logstash \
    && mkdir -p /usr/share/logstash \
    && chown -R 42478:42478 /usr/share/logstash



    

ENV JAVA_HOME /usr/lib/jvm/java-8-openjdk-amd64/



RUN apt-get update && apt-get -y install --no-install-recommends openjdk-8-jre-headless logrotate && apt-get clean && rm -rf /var/lib/apt/lists/*
COPY extend_start.sh /usr/local/bin/kolla_extend_start

# FIXME(dszumski): Logstash was added to Kolla for Monasca. Monasca is
# currently tied to an old messaging version in Kafka (0.9) and doesn't
# work with Logstash 5.x or above. When Monasca is updated to use a more
# recent messaging version this patch should be reverted and the Monasca
# Logstash configuration files upgraded to use the new format.


ENV logstash_deb_url=https://download.elastic.co/logstash/logstash/packages/debian/logstash-2.4.1_all.deb
ENV logstash_deb_sha1sum=7ba3b174a3ef48a7d0945d9b5c7f12c5005abb47
RUN curl -sSL -o /tmp/logstash.deb ${logstash_deb_url} \
    && echo "${logstash_deb_sha1sum} /tmp/logstash.deb" | sha1sum -c \
    && apt install /tmp/logstash.deb \
    && rm -f /tmp/logstash.deb



RUN chmod 755 /usr/local/bin/kolla_extend_start




USER logstash