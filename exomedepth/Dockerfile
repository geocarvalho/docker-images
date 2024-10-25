###############################################
# Dockerfile to build ExomeDepth scripts container image
#   chmod u+x ExomeDepth_cnv_calling.R ExomeDepth_count.R
#   docker build -t gvcn/r-exomedepth:v1.1.16 . --platform linux/amd64
#   docker push gvcn/r-exomedepth:v1.1.16
#   docker run -v $PWD:$PWD gvcn/r-exomedepth:v1.1.16 /home/bin/ExomeDepth_cnv_calling.R
#   docker run -v $PWD:$PWD gvcn/r-exomedepth:v1.1.16 /home/bin/ExomeDepth_count.R
###############################################
FROM quay.io/biocontainers/r-exomedepth:1.1.16--r43hfb3cda0_3
# Copy R script
ADD ExomeDepth_cnv_calling.R .
ADD ExomeDepth_count.R .
RUN mkdir /home/bin && \
    cp ExomeDepth_cnv_calling.R ExomeDepth_count.R /home/bin/

ENV PATH=/home/bin:${PATH}
