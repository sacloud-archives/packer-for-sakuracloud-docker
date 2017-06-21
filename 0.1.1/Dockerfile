FROM hashicorp/packer:latest
MAINTAINER Kazumichi Yamamoto <yamamoto.febc@gmail.com>

ENV PACKER_SAKURACLOUD_VERSION=0.1.1

ADD https://github.com/sacloud/packer-builder-sakuracloud/releases/download/v${PACKER_SAKURACLOUD_VERSION}/packer-builder-sakuracloud_linux-amd64.zip ./
RUN unzip packer-builder-sakuracloud_linux-amd64.zip -d /bin
RUN rm -f packer-builder-sakuracloud_linux-amd64.zip

VOLUME ["/work"]
WORKDIR /work

CMD ["--help"]
