FROM kolla/ubuntu-binary-nova-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="nova-ssh" build-date="20190404"








RUN usermod --append --home /var/lib/nova --groups kolla nova \
    && chsh --shell /bin/bash nova \
    && mkdir -p /var/lib/nova \
    && chown -R 42436:42436 /var/lib/nova






RUN mkdir -p /var/run/sshd \
    && chmod 0755 /var/run/sshd



RUN apt-get update && apt-get -y install --no-install-recommends openssh-server && apt-get clean && rm -rf /var/lib/apt/lists/*

RUN sed -ri 's/session(\s+)required(\s+)pam_loginuid.so/session\1optional\2pam_loginuid.so/' /etc/pam.d/sshd

COPY extend_start.sh /usr/local/bin/kolla_extend_start
RUN chmod 755 /usr/local/bin/kolla_extend_start


