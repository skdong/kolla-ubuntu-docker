FROM kolla/ubuntu-binary-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="storm" build-date="20190404"







RUN usermod --append --home /opt/storm --groups kolla storm \
    && mkdir -p /opt/storm \
    && chown -R 42479:42479 /opt/storm



    


RUN apt-get update && apt-get -y install --no-install-recommends openjdk-8-jre-headless && apt-get clean && rm -rf /var/lib/apt/lists/*


ENV storm_version=1.2.2
ENV storm_url=http://www.mirrorservice.org/sites/ftp.apache.org/storm/apache-storm-${storm_version}/apache-storm-${storm_version}.tar.gz
ENV storm_pkg_sha512sum=0a1120b8df7b22edc75f0a412d625841f72f3fb8e9ff5d413d510908d68ea1f0c17d68c1a7f1eda427b40902452e9efcae902c36499b558592e41cc1079de2e0



RUN curl -sSL -o /tmp/storm.tgz ${storm_url} \
    && echo "${storm_pkg_sha512sum} /tmp/storm.tgz" | sha512sum -c \
    && tar --strip 1 -xvf /tmp/storm.tgz -C /opt/storm \
    && rm -f /tmp/storm.tgz



COPY extend_start.sh /usr/local/bin/kolla_extend_start
RUN chmod 755 /usr/local/bin/kolla_extend_start




USER storm