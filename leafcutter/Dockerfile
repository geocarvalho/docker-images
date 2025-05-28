###############################################################
# Dockerfile to build container images for leafcutter v0.2.9
# Based on stephanholgerdrukewitz/leafcutter:latest
################################################################

FROM stephanholgerdrukewitz/leafcutter:latest

# Install classify_clusters.R
RUN cd /opt/leafcutter/leafcutter/leafcutter/R && \
wget https://raw.githubusercontent.com/davidaknowles/leafcutter/classify_clusters/leafviz/classify_clusters.R

# Set working directory
WORKDIR /home
