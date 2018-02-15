docker-keras
============

***docker-keras*** is a minimal [*Docker*](http://www.docker.com/) image built from *Debian 9* (amd64) for reproducible deep learning based on [*Keras*](http://keras.io/). It features minimal images for *Python 2 or 3*, [*TensorFlow*](http://www.tensorflow.org/), [*Theano*](http://deeplearning.net/software/theano/), or [*CNTK*](https://docs.microsoft.com/en-us/cognitive-toolkit/) backends, processing on CPU or GPU, and uses only Debian and Python packages (no manual installations). Each tag is using the latest released versions at a specific date.

Open source project:

- <i class="fa fa-fw fa-home"></i> home: <http://gw.tnode.com/docker/keras/>
- <i class="fa fa-fw fa-github-square"></i> github: <http://github.com/gw0/docker-keras/>
- <i class="fa fa-fw fa-laptop"></i> technology: *debian*, *keras*, *tensorflow*, *theano*, *cntk*, *cuda toolkit*, *openblas*, *python*, *numpy*, *h5py*
- <i class="fa fa-fw fa-database"></i> docker hub: <https://hub.docker.com/r/gw000/keras/>

Available tags:

- `2.1.4-py2`, `2.1.4-cpu`, `2.1.4`, `latest` points to `2.1.4-py2-tf-cpu`
- `2.1.4-py3` points to `2.1.4-py3-tf-cpu`
- `2.1.4-gpu` points to `2.1.4-py2-tf-gpu`
- `2.1.4-py2-tf-cpu`/`2.1.4-py2-tf-gpu`/`2.1.4-py3-tf-cpu`/`2.1.4-py3-tf-gpu` [2018-02-15]: *Python 2.7/3.5* + *Keras* <small>(2.1.4)</small> + *TensorFlow* <small>(1.5.0)</small> on CPU/GPU (*Dockerfile*[*.py2-tf-cpu*](http://github.com/gw0/docker-keras/blob/master/Dockerfile.py2-tf-cpu)/[*.py2-tf-gpu*](http://github.com/gw0/docker-keras/blob/master/Dockerfile.py2-tf-gpu)/[*.py3-tf-cpu*](http://github.com/gw0/docker-keras/blob/master/Dockerfile.py3-tf-cpu)/[*.py3-tf-gpu*](http://github.com/gw0/docker-keras/blob/master/Dockerfile.py3-tf-gpu))
- `2.1.4-py2-th-cpu`/`2.1.4-py2-th-gpu`/`2.1.4-py3-th-cpu`/`2.1.4-py3-th-gpu` [2018-02-15]: *Python 2.7/3.5* + *Keras* <small>(2.1.4)</small> + *Theano* <small>(1.0.1)</small> on CPU/GPU (*Dockerfile*[.py2-th-cpu*](http://github.com/gw0/docker-keras/blob/master/Dockerfile.py2-th-cpu)/[*.py2-th-gpu*](http://github.com/gw0/docker-keras/blob/master/Dockerfile.py2-th-gpu)[*.py3-th-cpu*](http://github.com/gw0/docker-keras/blob/master/Dockerfile.py3-th-cpu)/[*.py3-th-gpu*](http://github.com/gw0/docker-keras/blob/master/Dockerfile.py3-th-gpu))
- `2.1.4-py2-cntk-cpu`/`2.1.4-py2-cntk-gpu`/`2.1.4-py3-cntk-cpu`/`2.1.4-py3-cntk-gpu` [2018-02-15]: *Python 2.7/3.5* + *Keras* <small>(2.1.4)</small> + *CNTK* <small>(2.4)</small> on CPU/GPU (*Dockerfile*[.py2-cntk-cpu*](http://github.com/gw0/docker-keras/blob/master/Dockerfile.py2-cntk-cpu)/[*.py2-cntk-gpu*](http://github.com/gw0/docker-keras/blob/master/Dockerfile.py2-cntk-gpu)[*.py3-cntk-cpu*](http://github.com/gw0/docker-keras/blob/master/Dockerfile.py3-cntk-cpu)/[*.py3-cntk-gpu*](http://github.com/gw0/docker-keras/blob/master/Dockerfile.py3-cntk-gpu))
- `2.1.3-py2-tf-cpu`/`2.1.3-py2-tf-gpu`/`2.1.3-py3-tf-cpu`/`2.1.3-py3-tf-gpu` [2018-01-17]: *Python 2.7/3.5* + *Keras* <small>(2.1.3)</small> + *TensorFlow* <small>(1.4.1)</small> on CPU/GPU (*Dockerfile*[*.py2-tf-cpu*](http://github.com/gw0/docker-keras/blob/master/Dockerfile.py2-tf-cpu)/[*.py2-tf-gpu*](http://github.com/gw0/docker-keras/blob/master/Dockerfile.py2-tf-gpu)/[*.py3-tf-cpu*](http://github.com/gw0/docker-keras/blob/master/Dockerfile.py3-tf-cpu)/[*.py3-tf-gpu*](http://github.com/gw0/docker-keras/blob/master/Dockerfile.py3-tf-gpu))
- `2.1.3-py2-th-cpu`/`2.1.3-py2-th-gpu`/`2.1.3-py3-th-cpu`/`2.1.3-py3-th-gpu` [2018-01-17]: *Python 2.7/3.5* + *Keras* <small>(2.1.3)</small> + *Theano* <small>(1.0.1)</small> on CPU/GPU (*Dockerfile*[.py2-th-cpu*](http://github.com/gw0/docker-keras/blob/master/Dockerfile.py2-th-cpu)/[*.py2-th-gpu*](http://github.com/gw0/docker-keras/blob/master/Dockerfile.py2-th-gpu)[*.py3-th-cpu*](http://github.com/gw0/docker-keras/blob/master/Dockerfile.py3-th-cpu)/[*.py3-th-gpu*](http://github.com/gw0/docker-keras/blob/master/Dockerfile.py3-th-gpu))
- `2.1.3-py2-cntk-cpu`/`2.1.3-py2-cntk-gpu`/`2.1.3-py3-cntk-cpu`/`2.1.3-py3-cntk-gpu` [2018-01-17]: *Python 2.7/3.5* + *Keras* <small>(2.1.3)</small> + *CNTK* <small>(2.3)</small> on CPU/GPU (*Dockerfile*[.py2-cntk-cpu*](http://github.com/gw0/docker-keras/blob/master/Dockerfile.py2-cntk-cpu)/[*.py2-cntk-gpu*](http://github.com/gw0/docker-keras/blob/master/Dockerfile.py2-cntk-gpu)[*.py3-cntk-cpu*](http://github.com/gw0/docker-keras/blob/master/Dockerfile.py3-cntk-cpu)/[*.py3-cntk-gpu*](http://github.com/gw0/docker-keras/blob/master/Dockerfile.py3-cntk-gpu))
- `2.1.1-py2-tf-cpu`/`2.1.1-py2-tf-gpu`/`2.1.1-py3-tf-cpu`/`2.1.1-py3-tf-gpu` [2017-12-01]: *Python 2.7/3.5* + *Keras* <small>(2.1.1)</small> + *TensorFlow* <small>(1.4.0)</small> on CPU/GPU
- `2.1.1-py2-th-cpu`/`2.1.1-py2-th-gpu`/`2.1.1-py3-th-cpu`/`2.1.1-py3-th-gpu` [2017-12-01]: *Python 2.7/3.5* + *Keras* <small>(2.1.1)</small> + *Theano* <small>(1.0.0)</small> on CPU/GPU
- `2.1.1-py2-cntk-cpu`/`2.1.1-py2-cntk-gpu`/`2.1.1-py3-cntk-cpu`/`2.1.1-py3-cntk-gpu` [2017-12-01]: *Python 2.7/3.5* + *Keras* <small>(2.1.1)</small> + *CNTK* <small>(2.3)</small> on CPU/GPU
- `2.0.8-py2-tf-cpu`/`2.0.8-py2-tf-gpu`/`2.0.8-py3-tf-cpu`/`2.0.8-py3-tf-gpu` [2017-09-14]: *Python 2.7/3.5* + *Keras* <small>(2.0.8)</small> + *TensorFlow* <small>(1.3.0)</small> on CPU/GPU
- `2.0.8-py2-th-cpu`/`2.0.8-py2-th-gpu`/`2.0.8-py3-th-cpu`/`2.0.8-py3-th-gpu` [2017-09-14]: *Python 2.7/3.5* + *Keras* <small>(2.0.8)</small> + *Theano* <small>(0.9.0)</small> on CPU/GPU
- `2.0.8-py2-cntk-cpu`/`2.0.8-py2-cntk-gpu`/`2.0.8-py3-cntk-cpu`/`2.0.8-py3-cntk-gpu` [2017-09-14]: *Python 2.7/3.5* + *Keras* <small>(2.0.8)</small> + *CNTK* <small>(2.1)</small> on CPU/GPU
- `2.0.6-py2-tf-cpu`/`2.0.6-py2-tf-gpu`/`2.0.6-py3-tf-cpu`/`2.0.6-py3-tf-gpu` [2017-07-13]: *Python 2.7/3.5* + *Keras* <small>(2.0.6)</small> + *TensorFlow* <small>(1.2.1)</small> on CPU/GPU
- `2.0.6-py2-th-cpu`/`2.0.6-py2-th-gpu`/`2.0.6-py3-th-cpu`/`2.0.6-py3-th-gpu` [2017-07-13]: *Python 2.7/3.5* + *Keras* <small>(2.0.6)</small> + *Theano* <small>(0.9.0)</small> on CPU/GPU
- `2.0.5-py2-tf-cpu`/`2.0.5-py2-tf-gpu`/`2.0.5-py3-tf-cpu`/`2.0.5-py3-tf-gpu` [2017-06-13]: *Python 2.7/3.5* + *Keras* <small>(2.0.5)</small> + *TensorFlow* <small>(1.1.0)</small> on CPU/GPU
- `2.0.5-py2-th-cpu`/`2.0.5-py2-th-gpu`/`2.0.5-py3-th-cpu`/`2.0.5-py3-th-gpu` [2017-06-13]: *Python 2.7/3.5* + *Keras* <small>(2.0.5)</small> + *Theano* <small>(0.9.0)</small> on CPU/GPU
- `2.0.4-py2-tf-cpu`/`2.0.4-py2-tf-gpu`/`2.0.4-py3-tf-cpu`/`2.0.4-py3-tf-gpu` [2017-05-01]: *Python 2.7/3.5* + *Keras* <small>(2.0.4)</small> + *TensorFlow* <small>(1.1.0)</small> on CPU/GPU
- `2.0.4-py2-th-cpu`/`2.0.4-py2-th-gpu`/`2.0.4-py3-th-cpu`/`2.0.4-py3-th-gpu` [2017-05-01]: *Python 2.7/3.5* + *Keras* <small>(2.0.4)</small> + *Theano* <small>(0.9.0)</small> on CPU/GPU
- `2.0.3-py2-tf-cpu`/`2.0.3-py2-tf-gpu`/`2.0.3-py3-tf-cpu`/`2.0.3-py3-tf-gpu` [2017-04-19]: *Python 2.7/3.5* + *Keras* <small>(2.0.3)</small> + *TensorFlow* <small>(1.0.1)</small> on CPU/GPU
- `2.0.3-py2-th-cpu`/`2.0.3-py2-th-gpu`/`2.0.3-py3-th-cpu`/`2.0.3-py3-th-gpu` [2017-04-19]: *Python 2.7/3.5* + *Keras* <small>(2.0.3)</small> + *Theano* <small>(0.9.0)</small> on CPU/GPU
- `2.0.2-py2-tf-cpu`/`2.0.2-py2-tf-gpu`/`2.0.2-py3-tf-cpu`/`2.0.2-py3-tf-gpu` [2017-03-27]: *Python 2.7/3.5* + *Keras* <small>(2.0.2)</small> + *TensorFlow* <small>(1.0.1)</small> on CPU/GPU
- `2.0.2-py2-th-cpu`/`2.0.2-py2-th-gpu`/`2.0.2-py3-th-cpu`/`2.0.2-py3-th-gpu` [2017-03-27]: *Python 2.7/3.5* + *Keras* <small>(2.0.2)</small> + *Theano* <small>(0.9.0)</small> on CPU/GPU
- `2.0.0-py2-tf-cpu`/`2.0.0-py2-tf-gpu`/`2.0.0-py3-tf-cpu`/`2.0.0-py3-tf-gpu` [2017-03-15]: *Python 2.7/3.5* + *Keras* <small>(2.0.0)</small> + *TensorFlow* <small>(1.0.1)</small> on CPU/GPU
- `2.0.0-py2-th-cpu`/`2.0.0-py2-th-gpu`/`2.0.0-py3-th-cpu`/`2.0.0-py3-th-gpu` [2017-03-15]: *Python 2.7/3.5* + *Keras* <small>(2.0.0)</small> + *Theano* <small>(0.8.2)</small> on CPU/GPU
- `1.2.2-py2-tf-cpu`/`1.2.2-py2-tf-gpu`/`1.2.2-py3-tf-cpu`/`1.2.2-py3-tf-gpu` [2017-02-17]: *Python 2.7/3.5* + *Keras* <small>(1.2.2)</small> + *TensorFlow* <small>(1.0.0)</small> on CPU/GPU
- `1.2.2-py2-th-cpu`/`1.2.2-py2-th-gpu`/`1.2.2-py3-th-cpu`/`1.2.2-py3-th-gpu` [2017-02-17]: *Python 2.7/3.5* + *Keras* <small>(1.2.2)</small> + *Theano* <small>(0.8.2)</small> on CPU/GPU
- `1.2.1-py2-tf-cpu`/`1.2.1-py2-tf-gpu`/`1.2.1-py3-tf-cpu`/`1.2.1-py3-tf-gpu` [2017-01-20]: *Python 2.7/3.5* + *Keras* <small>(1.2.1)</small> + *TensorFlow* <small>(0.12.1)</small> on CPU/GPU
- `1.2.1-py2-th-cpu`/`1.2.1-py2-th-gpu`/`1.2.1-py3-th-cpu`/`1.2.1-py3-th-gpu` [2017-01-20]: *Python 2.7/3.5* + *Keras* <small>(1.2.1)</small> + *Theano* <small>(0.8.2)</small> on CPU/GPU
- `1.2.0-py2-tf-cpu`/`1.2.0-py2-tf-gpu`/`1.2.0-py3-tf-cpu`/`1.2.0-py3-tf-gpu` [2016-12-20]: *Python 2.7/3.5* + *Keras* <small>(1.2.0)</small> + *TensorFlow* <small>(0.12.0)</small> on CPU/GPU
- `1.2.0-py2-th-cpu`/`1.2.0-py2-th-gpu`/`1.2.0-py3-th-cpu`/`1.2.0-py3-th-gpu` [2016-12-20]: *Python 2.7/3.5* + *Keras* <small>(1.2.0)</small> + *Theano* <small>(0.8.2)</small> on CPU/GPU
- `1.1.1-py2-tf-cpu`/`1.1.1-py2-tf-gpu`/`1.1.1-py3-tf-cpu`/`1.1.1-py3-tf-gpu` [2016-10-31]: *Python 2.7/3.5* + *Keras* <small>(1.1.1)</small> + *TensorFlow* <small>(0.10.0)</small> on CPU/GPU
- `1.1.1-py2-th-cpu`/`1.1.1-py2-th-gpu`/`1.1.1-py3-th-cpu`/`1.1.1-py3-th-gpu` [2016-10-31]: *Python 2.7/3.5* + *Keras* <small>(1.1.1)</small> + *Theano* <small>(0.8.2)</small> on CPU/GPU
- `1.1.0-py2-tf-cpu`/`1.1.0-py2-tf-gpu`/`1.1.0-py3-tf-cpu`/`1.1.0-py3-tf-gpu` [2016-09-20]: *Python 2.7/3.5* + *Keras* <small>(1.1.0)</small> + *TensorFlow* <small>(0.10.0)</small> on CPU/GPU
- `1.1.0-py2-th-cpu`/`1.1.0-py2-th-gpu`/`1.1.0-py3-th-cpu`/`1.1.0-py3-th-gpu` [2016-09-20]: *Python 2.7/3.5* + *Keras* <small>(1.1.0)</small> + *Theano* <small>(0.8.2)</small> on CPU/GPU
- `1.0.8-py2-tf-cpu`/`1.0.8-py2-tf-gpu`/`1.0.8-py3-tf-cpu`/`1.0.8-py3-tf-gpu` [2016-08-28]: *Python 2.7/3.5* + *Keras* <small>(1.0.8)</small> + *TensorFlow* <small>(0.9.0)</small> on CPU/GPU
- `1.0.8-py2-th-cpu`/`1.0.8-py2-th-gpu`/`1.0.8-py3-th-cpu`/`1.0.8-py3-th-gpu` [2016-08-28]: *Python 2.7/3.5* + *Keras* <small>(1.0.8)</small> + *Theano* <small>(0.8.2)</small> on CPU/GPU
- `1.0.6-py2-tf-cpu`/`1.0.6-py2-tf-gpu`/`1.0.6-py3-tf-cpu`/`1.0.6-py3-tf-gpu` [2016-07-20]: *Python 2.7/3.5* + *Keras* <small>(1.0.6)</small> + *TensorFlow* <small>(0.9.0)</small> on CPU/GPU
- `1.0.6-py2-th-cpu`/`1.0.6-py2-th-gpu`/`1.0.6-py3-th-cpu`/`1.0.6-py3-th-gpu` [2016-07-20]: *Python 2.7/3.5* + *Keras* <small>(1.0.6)</small> + *Theano* <small>(0.8.2)</small> on CPU/GPU
- `1.0.4-py2-tf-cpu`/`1.0.4-py2-tf-gpu`/`1.0.4-py3-tf-cpu`/`1.0.4-py3-tf-gpu` [2016-06-16]: *Python 2.7/3.5* + *Keras* <small>(1.0.4)</small> + *TensorFlow* <small>(0.8.0)</small> on CPU/GPU
- `1.0.4-py2-th-cpu`/`1.0.4-py2-th-gpu`/`1.0.4-py3-th-cpu`/`1.0.4-py3-th-gpu` [2016-06-16]: *Python 2.7/3.5* + *Keras* <small>(1.0.4)</small> + *Theano* <small>(0.8.2)</small> on CPU/GPU
- `1.0.1-py2-th-cpu`/`1.0.1-py2-th-gpu` [2016-04-16]: *Python 2.7* + *Keras* <small>(1.0.1)</small> + *Theano* <small>(0.8.1)</small> on CPU/GPU
- `0.3.3-py2-th-cpu`/`0.3.3-py2-th-gpu` [2016-03-31]: *Python 2.7* + *Keras* <small>(0.3.3)</small> + *Theano* <small>(0.8.1)</small> on CPU/GPU


Usage
=====

Quick experiment with latest Keras (with TensorFlow backend on CPU) and your Python 2 code in current directory (will be mapped to `/srv`):

```bash
$ docker run -it --rm -v $(pwd):/srv gw000/keras /srv/run.py
```

Or using TensorFlow backend on GPUs in Python 2 (see [docker-debian-cuda](http://gw.tnode.com/docker/debian-cuda/)):

```bash
$ docker run -it --rm $(ls /dev/nvidia* | xargs -I{} echo '--device={}') $(ls /usr/lib/*-linux-gnu/{libcuda,libnvidia}* | xargs -I{} echo '-v {}:{}:ro') -v $(pwd):/srv gw000/keras:2.1.4-py2-tf-gpu /srv/run.py
```

Or using Theano backend on GPUs in Python 3 (see [docker-debian-cuda](http://gw.tnode.com/docker/debian-cuda/)):

```bash
$ docker run -it --rm $(ls /dev/nvidia* | xargs -I{} echo '--device={}') $(ls /usr/lib/*-linux-gnu/{libcuda,libnvidia}* | xargs -I{} echo '-v {}:{}:ro') -v $(pwd):/srv gw000/keras:2.1.4-py3-th-gpu /srv/run.py
```

Additional parameters in above commands explicitly expose your GPU devices and CUDA Driver library from the host system into the container. The vendor specific *nvidia-docker* tool performs the same thing in a less transparent way and is incompatible with other Docker tools. For more instructions see [docker-debian-cuda](http://gw.tnode.com/docker/debian-cuda/).

In practice you are supposed to extend this image by writing your own `Dockerfile` that installs all your application dependencies (either using `apt-get` or `pip`). Eg. if you need Matplotlib, PIL/pillow, Pandas, Scikit-learn, and Statsmodels:

```
FROM gw000/keras:2.1.4-py3-tf-cpu

# install dependencies from debian packages
RUN apt-get update -qq \
 && apt-get install --no-install-recommends -y \
    python-matplotlib \
    python-pillow

# install dependencies from python packages
RUN pip --no-cache-dir install \
    pandas \
    scikit-learn \
    statsmodels

# install your app
ADD ai/ /srv/ai/
RUN chmod +x /srv/ai/run.py

# default command
CMD ["/srv/ai/run.py"]
```

If you are looking for a full deep learning research environment based on *Keras* and *Jupyter*, check out [docker-keras-full](http://gw.tnode.com/docker/keras-full/).


Feedback
========

If you encounter any bugs or have feature requests, please file them in the [issue tracker](http://github.com/gw0/docker-keras/issues/) or even develop it yourself and submit a pull request over [GitHub](http://github.com/gw0/docker-keras/).


License
=======

Copyright &copy; 2016-2018 *gw0* [<http://gw.tnode.com/>] &lt;<gw.2018@ena.one>&gt;

All code is licensed under the [GNU Affero General Public License 3.0+](LICENSE_AGPL-3.0.txt) (AGPL-3.0+). Note that it is mandatory to make all modifications and complete source code publicly available to any user.
