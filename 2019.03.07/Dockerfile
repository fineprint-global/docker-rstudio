FROM rocker/rstudio:3.5.2 
MAINTAINER "Victor Maus" victor.maus@wu.ac.at

RUN apt-get update \
  && apt-get install -y --no-install-recommends \
    ## Dependencies from rocker/geospatial
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
  && R CMD javareconf \
  && install2.r --error \
    BiocManager \
    ## from bioconductor
  && R -e "BiocManager::install('rhdf5', ask = FALSE)" \ 
  && install2.r --error \
    ## R packages from rocker/geospatial
    tidyverse \
    curl \
    XML \
    xml2 \
    readxl \
    rio \
    bookdown \
    RColorBrewer \
    RandomFields \
    RNetCDF \
    classInt \
    deldir \
    gstat \
    hdf5r \
    lidR \
    mapdata \
    maptools \
    mapview \
    ncdf4 \
    proj4 \
    raster \
    rgdal \
    rgeos \
    rlas \
    sf \
    sp \
    spacetime \
    spatstat \
    spdep \
    geoR \
    geosphere \
    ## Additional R packages 
    devtools \
    roxygen2 \
    RSelenium \
    rlist \
    ggthemes \
    ggmosaic \
    viridis \
    XLConnect \
    ckanr \
    ggrepel \
    ggmap \
    kableExtra \
    countrycode \
    gsubfn \
    rmapshaper \
    readODS \
    caret \
    RWeka \
    config \
    dendextend \
    ensurer \
    dtw \
    dtwclust \
    dtwSat \
    reticulate \
    gbm \
    keras \
    kohonen \
    imputeTS \
    log4r \
    openxlsx \
    ranger \
    signal \
    wtss \
    comtradr \
    xlsx \
    captioner \
    stargazer \
    getPass \
    MODIS
 
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




