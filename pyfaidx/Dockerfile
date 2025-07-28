###############################################
# Dockerfile to pyfaidx container image
#   docker build -t gvcn/pyfaidx:v1.0 . --platform linux/amd64
#   docker push gvcn/pyfaidx:v1.0
#   docker run -v $PWD:$PWD gvcn/pyfaidx:v1.0 python /path/to/bed2vcf.py -h
###############################################
FROM continuumio/miniconda3:latest
# Install git
RUN conda install -c anaconda git -y --quiet && \
    conda install bioconda::pyfaidx -y 
