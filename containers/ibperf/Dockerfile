#ib perf test docker file, based on ubuntu 22.04
# Oct 2024, lazyelectrons
# ghcr.io/lazyelectrons/ibperf:latest
FROM ubuntu:22.04
# Ubuntu 22.04 docker container with inbox Mellanox drivers
# LABEL about the custom image
LABEL maintainer=github.com/lazyelectrons
#LABEL org.opencontainers.image.source=https://github.com/octocat/my-repo
LABEL org.opencontainers.image.description="This is custom Container with the latest IB perftest package"
WORKDIR /tmp/
ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get clean -y && apt-get -y update && apt-get install -y apt-utils udev vim bash && apt-get -y upgrade
RUN apt-get install -y  build-essential manpages-dev git iputils-ping traceroute tcpdump iproute2   
RUN apt-get install -y iproute2 rdma-core libibmad5 ibutils ibverbs-utils infiniband-diags mstflint strace iputils-ping
RUN apt-get install -y libtool  libibverbs-dev libibverbs-dev librdmacm-dev libibumad-dev libpci-dev infiniband-diags ibutils ibverbs-utils rdmacm-utils
RUN apt-get install iperf3 -y
RUN git clone  https://github.com/linux-rdma/perftest
RUN cd perftest && ./autogen.sh && ./configure && make -j 4 && make install
RUN dpkg-reconfigure --frontend noninteractive tzdata && apt-get clean all -y
WORKDIR /root/
ENTRYPOINT ["tail", "-f", "/dev/null"]
