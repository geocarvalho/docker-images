###############################################
# Dockerfile to build pypgx container image
#   docker build -t pypgx:v0.15.0 .
#   docker run -v "$PWD":/data pypgx:v0.15.0 pypgx --version
###############################################
FROM continuumio/miniconda3:4.9.2-alpine

WORKDIR /root

# Install git
RUN apk update && \
    apk add git && \
    git clone --branch 0.15.0 --depth 1 https://github.com/sbslee/pypgx-bundle

# Create the environment:
COPY environment.yml .
RUN conda env create -f environment.yml

# The code to run when container is started:
ENTRYPOINT ["conda", "run", "-n", "myenv"]
CMD ["conda", "run", "-n", "myenv", "pypgx", "-h"]
