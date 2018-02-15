# docker-keras - Keras in Docker with Python 3 and Theano on GPU

FROM gw000/debian-cuda:9.1_7.0
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
    # install python 3
    python3 \
    python3-dev \
    python3-pip \
    python3-setuptools \
    python3-virtualenv \
    python3-wheel \
    pkg-config \
    # requirements for numpy
    libopenblas-base \
    python3-numpy \
    python3-scipy \
    # requirements for keras
    python3-h5py \
    python3-yaml \
    python3-pydot \
    # requirements for theano
    cmake \
    cython3 \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

# build and install requirements for theano
RUN git clone https://github.com/Theano/libgpuarray.git /tmp/libgpuarray \
 && cd /tmp/libgpuarray \
 && mkdir ./Build \
 && cd ./Build \
 && cmake .. -DCMAKE_BUILD_TYPE=Release \
 && make \
 && make install \
 && cd .. \
 && python3 setup.py build \
 && python3 setup.py install \
 && cd / \
 && rm -rf /tmp/libgpuarray \
 && ldconfig

ARG THEANO_VERSION=1.0.1
ENV THEANO_FLAGS='device=cuda,floatX=float32'
RUN pip3 --no-cache-dir install git+https://github.com/Theano/Theano.git@rel-${THEANO_VERSION}

ARG KERAS_VERSION=2.1.4
ENV KERAS_BACKEND=theano
RUN pip3 --no-cache-dir install --no-dependencies git+https://github.com/fchollet/keras.git@${KERAS_VERSION}

# quick test and dump package lists
RUN python3 -c "import theano; print(theano.__version__)" \
 && dpkg-query -l > /dpkg-query-l.txt \
 && pip3 freeze > /pip3-freeze.txt

WORKDIR /srv/
