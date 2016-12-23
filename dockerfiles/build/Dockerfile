FROM jbernhard/hic-base

RUN apt-get update && apt-get install --yes --no-install-recommends \
    gcc \
    g++ \
    gfortran \
    make \
    cmake \
    libboost-dev \
    libboost-filesystem-dev \
    libboost-program-options-dev \
    libhdf5-dev \
    python3-dev \
    python3-pip \
    python3-setuptools \
    cython3 \
  && rm -rf /var/lib/apt/lists/*

# frzout is a build dependency because it generates the HRG part of the equation
# of state for vishnew, so install it with pip from a github-generated tar.  pip
# can install directly from git repos, but this way git (and all its
# dependencies) need not be installed.
RUN pip3 install --disable-pip-version-check --verbose \
  https://github.com/jbernhard/frzout/archive/master.tar.gz
