###############################################
# Dockerfile to build pypgx container image
# Based on Miniconda3
# Build with:
#   docker build -t pypgx:v0.15.0 .
# Run with:
#   docker run pypgx:v0.15.0 --version
###############################################
FROM continuumio/miniconda3:4.9.2-alpine

WORKDIR /app

# Install git
RUN apk update && \
    apk add git && \
    git clone --branch 0.15.0 --depth 1 https://github.com/sbslee/pypgx-bundle

# Create the environment:
COPY environment.yml .
RUN conda env create -f environment.yml

# Make RUN commands use the new environment:
SHELL ["conda", "run", "-n", "myenv", "/bin/bash", "-c"]

# The code to run when container is started:
ENTRYPOINT ["conda", "run", "-n", "myenv", "pypgx"]
