FROM kolla/ubuntu-binary-keystone-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="keystone-fernet" build-date="20190404"






    

RUN apt-get update && apt-get -y install --no-install-recommends cron openssh-client rsync && apt-get clean && rm -rf /var/lib/apt/lists/*

COPY fetch_fernet_tokens.py /usr/bin/
COPY keystone_bootstrap.sh /usr/local/bin/kolla_keystone_bootstrap
COPY extend_start.sh /usr/local/bin/kolla_extend_start
RUN chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_keystone_bootstrap /usr/bin/fetch_fernet_tokens.py


