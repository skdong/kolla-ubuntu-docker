FROM kolla/ubuntu-binary-bifrost-base:8.0.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="bifrost-deploy" build-date="20190404"



ENV container docker





# derived from https://raw.githubusercontent.com/tianon/dockerfiles/4d24a12b54b75b3e0904d8a285900d88d3326361/sbin-init/ubuntu/upstart/14.04/Dockerfile
ADD init-fake.conf /etc/init/fake-container-events.conf

# undo some leet hax of the base image
RUN rm /usr/sbin/policy-rc.d; \
    rm /sbin/initctl; dpkg-divert --rename --remove /sbin/initctl

# remove some pointless services
RUN /usr/sbin/update-rc.d -f ondemand remove; \
    for f in \
        /etc/init/u*.conf \
        /etc/init/mounted-dev.conf \
        /etc/init/mounted-proc.conf \
        /etc/init/mounted-run.conf \
        /etc/init/mounted-tmp.conf \
        /etc/init/mounted-var.conf \
        /etc/init/hostname.conf \
        /etc/init/networking.conf \
        /etc/init/tty*.conf \
        /etc/init/plymouth*.conf \
        /etc/init/hwclock*.conf \
        /etc/init/module*.conf\
    ; do \
        dpkg-divert --local --rename --add "$f"; \
    done; \
    echo '# /lib/init/fstab: cleared out for bare-bones Docker' > /lib/init/fstab




RUN apt-get update && apt-get -y install --no-install-recommends e2fsprogs && apt-get clean && rm -rf /var/lib/apt/lists/*

# Clear any customisation by Kolla to entrypoint & command
ENTRYPOINT []
CMD [ "/sbin/init" ]


