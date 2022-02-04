# docker build -t fastp:0.23.2 .
# docker run fastp:0.23.2 --version
# work from latest LTS ubuntu release
FROM ubuntu:18.04

# run update and install necessary tools
RUN apt-get update -y && apt-get install -y \
build-essential \
libnss-sss \
curl \
vim \
less \
wget \
unzip \
zlib1g-dev

# install fastp
WORKDIR /usr/local/bin/
RUN wget http://opengene.org/fastp/fastp.0.23.2 && mv fastp.0.23.2 fastp && chmod a+x ./fastp
ENTRYPOINT ["fastp"]
