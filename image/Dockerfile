
FROM cirepo/nix:2.1.1-bionic


ARG IMAGE_ARG_APT_MIRROR


COPY --chown=ubuntu:ubuntu docker /data


RUN set -ex \
  && sudo sed -i "s/http:\/\/archive.ubuntu.com\/ubuntu\//http:\/\/${IMAGE_ARG_APT_MIRROR:-archive.ubuntu.com}\/ubuntu\//g" /etc/apt/sources.list \
  && sudo apt-get -y update \
  && sudo apt-get -y install graphviz \
  && sudo apt-get -q -y autoremove \
  && sudo apt-get -q -y clean && sudo rm -rf /tmp/* && sudo rm -rf /var/cache && sudo rm -rf /var/lib/apt && sudo rm -rf /var/log \
  && sudo mkdir -p /var/cache/apt/archives/partial && sudo mkdir -p /var/log/apt \
  && touch /tmp/graphviz
