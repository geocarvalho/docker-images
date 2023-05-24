# docker build -t gvcn/star:2.7.10b .
# docker run gvcn/star:2.7.10b STAR --help
FROM debian:stable-slim

ARG STAR_VERSION=2.7.10b

ENV PACKAGES gcc g++ make wget zlib1g-dev unzip

RUN set -ex

RUN apt-get update && \
    apt-get install -y --no-install-recommends ${PACKAGES} && \
    apt-get clean && \
    g++ --version && \
    cd /home && \
    wget --no-check-certificate https://github.com/alexdobin/STAR/archive/${STAR_VERSION}.zip && \
    unzip ${STAR_VERSION}.zip && \
    cd STAR-${STAR_VERSION}/source && \
    make CXXFLAGS_SIMD=-std=c++11 STARstatic && \
    mkdir /home/bin && \
    cp STAR /home/bin && \
    cd /home && \
    'rm' -rf STAR-${STAR_VERSION} && \
    apt-get --purge autoremove -y  ${PACKAGES}

ENV PATH /home/bin:${PATH}
