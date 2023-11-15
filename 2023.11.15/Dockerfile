FROM rocker/rstudio:4.3.2 

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
    libv8-dev \
    libnode-dev \
    libcairo2-dev \
    libgit2-dev \
    r-cran-openssl \
    r-base-dev \
    r-cran-rjava \
    liblzma-dev \
    openjdk-11-jre \
    openjdk-11-jdk \
    libpcre3-dev \
    python-gdal \
    libjq-dev \
    libprotobuf-dev \
    libprotoc-dev \
    protobuf-compiler \
    r-cran-ncdf4 

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
