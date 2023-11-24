FROM registry.access.redhat.com/ubi8/ubi
USER root
LABEL maintainer="John Doe"

ENV BUILD_DEPS='libica-utils openssl libssl-dev openssl-ibmca time s390-tools opencryptoki'

# Update image/install pkgs
RUN yum update --disablerepo=* --enablerepo=ubi-8-appstream-rpms --enablerepo=ubi-8-baseos-rpms -y && rm -rf /var/cache/yum
RUN yum install --disablerepo=* --enablerepo=ubi-8-appstream-rpms --enablerepo=ubi-8-baseos-rpms $BUILD_DEPS -y && rm -rf /var/cache/yum

CMD ["/bin/bash", "-c", "sleep infinity"]
