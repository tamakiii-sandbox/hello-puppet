FROM --platform=linux/amd64 amazonlinux:2.0.20221103.3

RUN yum update && \
    amazon-linux-extras enable \
      ruby2.6 \
      && \
    yum install -y \
      which \
      make \
      ruby \
      && \
    yum clean all && \
    rm -rf /var/cache/yum/*

COPY Makefile /tmp/Makefile
RUN make -C /tmp install && \
    rm -rf /tmp/Makefile

CMD ["tail", "-f", "/dev/null"]
