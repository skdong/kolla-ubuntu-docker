FROM kolla/ubuntu-binary-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="zookeeper" build-date="20190404"







RUN usermod --append --home /opt/zookeeper --groups kolla zookeeper \
    && mkdir -p /opt/zookeeper \
    && chown -R 42453:42453 /opt/zookeeper



    


RUN apt-get update && apt-get -y install --no-install-recommends default-jre-headless && apt-get clean && rm -rf /var/lib/apt/lists/*


ENV zookeeper_version=3.4.13
ENV zookeeper_url=http://archive.apache.org/dist/zookeeper/zookeeper-${zookeeper_version}/zookeeper-${zookeeper_version}.tar.gz
ENV zookeeper_pkg_sha1sum=a989b527f3f990d471e6d47ee410e57d8be7620b



RUN curl -sSL -o /tmp/zookeeper.tar.gz ${zookeeper_url} \
    && echo "${zookeeper_pkg_sha1sum} /tmp/zookeeper.tar.gz" | sha1sum -c \
    && tar --strip 1 -xvf /tmp/zookeeper.tar.gz -C /opt/zookeeper \
    && rm -f /tmp/zookeeper.tar.gz


COPY extend_start.sh /usr/local/bin/kolla_extend_start
RUN chmod 755 /usr/local/bin/kolla_extend_start




USER zookeeper