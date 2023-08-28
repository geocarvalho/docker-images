# docker build -t bwamem2_samtools:1.0.0 .
# docker run -v $PWD:$PWD bwamem2_samtools:1.0.0 bwa-mem2
# docker run -v $PWD:$PWD bwamem2_samtools:1.0.0 samtools
# https://docs.docker.com/build/building/multi-stage/

FROM quay.io/biocontainers/samtools:1.3.1--h0cf4675_11

COPY --from=quay.io/biocontainers/bwa-mem2:2.2.1--hd03093a_4 /usr/local/bin/bwa-mem2* /usr/local/bin/
