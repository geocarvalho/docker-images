# docker build -t gvcn/bwa-mem2_biobambam:2.2.1_2.0.183 .
# docker run -v $PWD:$PWD gvcn/bwa-mem2_biobambam:2.2.1_2.0.183 bwa-mem2
# docker run -v $PWD:$PWD gvcn/bwa-mem2_biobambam:2.2.1_2.0.183 bamsormadup
# https://docs.docker.com/build/building/multi-stage/

FROM quay.io/biocontainers/biobambam:2.0.183--h4ac6f70_3

COPY --from=quay.io/biocontainers/bwa-mem2:2.2.1--hd03093a_4 /usr/local/bin/bwa-mem2* /usr/local/bin/
