FROM rocker/rstudio:3.6.3 
MAINTAINER "Victor Maus" victor.maus@wu.ac.at

# REMOVE as soon as Debian Buster is used! ---
# Use buster-repository for libgeos-dev
RUN echo "deb http://ftp.de.debian.org/debian buster main" > /etc/apt/sources.list.d/backports.list
RUN printf "# Do not use this\nPackage: *\nPin: release v=10.1\nPin-Priority: 1\n\n# Except for libgeos-dev\nPackage: libgeos-dev\nPin: release v=10.1\nPin-Priority: 500\n\nPackage: libgeos-c1v5\nPin: release v=10.1\nPin-Priority: 500\n" > /etc/apt/preferences.d/9_buster
# ---

RUN apt-get update \
  && apt-get install -y --no-install-recommends \
    ## Dependencies from rocker/geospatial
    libmagick++-dev \
    libxml2 \
    libxml2-dev \
    lbzip2 \
    libbz2-dev \
    libfftw3-dev \
    libgdal-dev \
    libgeos-dev \
    libgsl0-dev \
    libgl1-mesa-dev \
    libglu1-mesa-dev \
    libhdf4-alt-dev \
    libhdf5-dev \
    libjq-dev \
    liblwgeom-dev \
    libproj-dev \
    libprotobuf-dev \
    libnetcdf-dev \
    libsqlite3-dev \
    libssl-dev \
    libudunits2-dev \
    netcdf-bin \
    protobuf-compiler \
    tk-dev \
    unixodbc-dev \
    ## Additional dependencies
    gdal-bin \
    proj-bin \
    libnlopt-dev \
    libv8-3.14-dev \
    libcairo2-dev \
    libgit2-dev \
    r-cran-openssl \
    r-base-dev \
    r-cran-rjava \
    liblzma-dev \
    openjdk-8-jre \
    openjdk-8-jdk \
    libpcre3-dev \
    python-gdal \
    libjq-dev \
    libprotobuf-dev \
    libprotoc-dev \
    protobuf-compiler \
    r-cran-ncdf4 \
    libv8-3.14-dev

RUN install2.r --error \
    ## R packages from rocker/geospatial
    tidyverse \
    curl \
    xml2 \
    bookdown \
    RColorBrewer \
    raster \
    rgdal \
    rgeos \
    sf \
    sp \
    ## Additional R packages 
    devtools \
    viridis \
    ckanr \
    countrycode \
    reticulate \
    keras \
    getPass
 
RUN apt-get update \
  && apt-get install -y --no-install-recommends \
    ## Other system util tools  
    htop \
    cifs-utils \
    nfs-common \
    curl \
    vim \
    nano \
    openssh-client

RUN curl -sL https://deb.nodesource.com/setup_12.x | bash - \
  && apt-get install -y --no-install-recommends \
   nodejs \
  && npm install -g mapshaper
