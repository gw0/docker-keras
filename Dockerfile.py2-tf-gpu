# docker-keras - Keras in Docker with Python 2 and TensorFlow on GPU

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
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

# manually update numpy
RUN pip --no-cache-dir install -U numpy==1.13.3

ARG TENSORFLOW_VERSION=1.5.0
ARG TENSORFLOW_DEVICE=gpu
ARG TENSORFLOW_APPEND=_gpu
RUN pip --no-cache-dir install https://storage.googleapis.com/tensorflow/linux/${TENSORFLOW_DEVICE}/tensorflow${TENSORFLOW_APPEND}-${TENSORFLOW_VERSION}-cp27-none-linux_x86_64.whl

ARG KERAS_VERSION=2.1.4
ENV KERAS_BACKEND=tensorflow
RUN pip --no-cache-dir install --no-dependencies git+https://github.com/fchollet/keras.git@${KERAS_VERSION}

# quick test and dump package lists
RUN python -c "import tensorflow; print(tensorflow.__version__)" \
 && dpkg-query -l > /dpkg-query-l.txt \
 && pip2 freeze > /pip2-freeze.txt

WORKDIR /srv/
