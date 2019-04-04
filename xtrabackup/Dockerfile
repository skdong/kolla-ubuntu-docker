FROM kolla/ubuntu-binary-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="xtrabackup" build-date="20190404"








    


RUN apt-get update && apt-get -y install --no-install-recommends percona-xtrabackup-24 qpress && apt-get clean && rm -rf /var/lib/apt/lists/*

COPY backup.sh /usr/local/bin/kolla_mariadb_backup.sh
RUN chmod 755 /usr/local/bin/kolla_mariadb_backup.sh

CMD /usr/local/bin/kolla_mariadb_backup.sh


