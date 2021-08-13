# FROM debian:stretch-20200803 AS base
FROM continuumio/miniconda3:4.9.2-alpine

# Install git
RUN conda install -c anaconda git && conda install -c conda-forge mamba

# Build Pangolin (v3.1.11)
# FROM base as pangolin
RUN git clone --branch v3.1.11 --depth 1 https://github.com/cov-lineages/pangolin.git && \
    cd pangolin && \
    mamba env update --name base --file environment.yml --prune && \
    pip install .