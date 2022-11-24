FROM amazonlinux:2.0.20221103.3

RUN yum update && \
    yum install -y \
      which \
      make \
      && \
    yum clean all && \
    rm -rf /var/cache/yum/*

COPY Makefile /tmp/Makefile

RUN make -C /tmp install && \
    rm -rf /tmp/Makefile

CMD ["/opt/puppetlabs/bin/puppetserver", "start"]
