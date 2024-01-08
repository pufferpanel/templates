FROM steamcmd/steamcmd

ARG aptproxy=""
ENV DEBIAN_FRONTEND=noninteractive

RUN if [ -n "${aptproxy}" ]; then echo "Acquire::http::Proxy \"http://${aptproxy}\";" > /etc/apt/apt.conf.d/00-apt-proxy; fi && \
    apt-get update && \
    apt-get install -y libtinfo5:i386 libncurses5:i386 libcurl3-gnutls:i386 && \
    apt-get clean && \
    rm -rf /var/cache/apt/archives