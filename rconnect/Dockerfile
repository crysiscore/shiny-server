FROM  debian:11.5-slim

# install R package dependencies
RUN apt-get update && apt-get -qq -y install curl \
    libssl-dev \
    libcurl4-openssl-dev \
    ## clean up
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/ \
    && rm -rf /tmp/downloaded_packages/ /tmp/*.rds
   
RUN apt-get update && apt-get install -y \
    sudo \
    pandoc \
    pandoc-citeproc \
    libcurl4-gnutls-dev \
    libcairo2-dev \
    libxt-dev \
    libssh2-1-dev

# select port
EXPOSE 3838
# run app
