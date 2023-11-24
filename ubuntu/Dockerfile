# simple dockerfile to test OCP s2i using Dockerfile 

#FROM ubuntu:18.04
FROM ubi8/ubi

ENV BUILD_DEPS='libica-utils openssl libssl-dev openssl-ibmca time s390-tools opencryptoki'

RUN set -x \
&&  dnf update -y\
&&  dnf install -y $BUILD_DEPS 

CMD ["/bin/bash", "-c", "sleep infinity"]
# CMD ["/bin/bash", "-c", "--", "while true; do sleep 30; done;"]
