# docker-keras - Keras in Docker with Python 2 and CNTK on CPU

FROM debian:stretch
MAINTAINER gw0 [http://gw.tnode.com/] <gw.2018@ena.one>

# install debian packages
ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update -qq \
 && apt-get install --no-install-recommends -y \
    # install essentials
    build-essential \
    g++ \
    git \
    openssh-client \
    # install python 2
    python \
    python-dev \
    python-pip \
    python-setuptools \
    python-virtualenv \
    python-wheel \
    pkg-config \
    # requirements for numpy
    libopenblas-base \
    python-numpy \
    python-scipy \
    # requirements for keras
    python-h5py \
    python-yaml \
    python-pydot \
    # other repositories
    ubuntu-archive-keyring \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

# install from old ubuntu repositories for cntk
RUN echo 'deb http://archive.ubuntu.com/ubuntu/ xenial main restricted universe multiverse' > /etc/apt/sources.list.d/ubuntu-16.04.list
RUN apt-get update -qq \
 && apt-get install --no-install-recommends -y \
    # requirements for cntk
    openmpi-bin=1.10.2-8ubuntu1 \
    openmpi-common=1.10.2-8ubuntu1 \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

ARG CNTK_VERSION=2.4
ARG CNTK_DEVICE=CPU-Only
RUN pip --no-cache-dir install https://cntk.ai/PythonWheel/${CNTK_DEVICE}/cntk-${CNTK_VERSION}-cp27-cp27mu-linux_x86_64.whl

ARG KERAS_VERSION=2.1.4
ENV KERAS_BACKEND=cntk
RUN pip --no-cache-dir install --no-dependencies git+https://github.com/fchollet/keras.git@${KERAS_VERSION}

# quick test and dump package lists
RUN python -c "import cntk; print(cntk.__version__)" \
 && dpkg-query -l > /dpkg-query-l.txt \
 && pip2 freeze > /pip2-freeze.txt

WORKDIR /srv/
