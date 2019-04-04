FROM kolla/ubuntu-binary-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="openstack-base" build-date="20190404"






    

# This will prevent questions from being asked during the install
ENV DEBIAN_FRONTEND noninteractive
        
    

RUN apt-get update && apt-get -y install --no-install-recommends openssl patch python-aodhclient python-barbicanclient python-congressclient python-designateclient python-elasticsearch python-etcd python-gnocchiclient python-heatclient python-ironicclient python-kazoo python-keystoneclient python-magnumclient python-manilaclient python-memcache python-mistralclient python-muranoclient python-mysqldb python-openstackclient python-oslo.log python-osprofiler python-pip python-psycopg2 python-pymemcache python-pymysql python-redis python-saharaclient python-sysv-ipc python-swiftclient python-troveclient python-zake python-zaqarclient && apt-get clean && rm -rf /var/lib/apt/lists/*



