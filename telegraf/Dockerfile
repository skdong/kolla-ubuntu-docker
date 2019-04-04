FROM kolla/ubuntu-binary-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="telegraf" build-date="20190404"







RUN usermod --append --home /etc/telegraf --groups kolla telegraf \
    && mkdir -p /etc/telegraf \
    && chown -R 42448:42448 /etc/telegraf





    


RUN apt-get update && apt-get -y install --no-install-recommends chrony net-tools telegraf collectd-core python-pip && apt-get clean && rm -rf /var/lib/apt/lists/*

COPY telegraf_sudoers /etc/sudoers.d/kolla_telegraf_sudoers
COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN chmod 750 /etc/sudoers.d \
    && chmod 440 /etc/sudoers.d/kolla_telegraf_sudoers \
    && chmod 755 /usr/local/bin/kolla_extend_start




USER telegraf