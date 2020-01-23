FROM tensorflow/tensorflow:1.8.0-gpu
MAINTAINER Guang Yang <garry.yangguang@gmail.com>

RUN apt-get update -y && apt-get install -y \
  sox \
  libsndfile1-dev \
  git \
  ffmpeg \
  tk-dev \
  python-tk \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*


ADD pip-requirements.txt /pip-requirements.txt
RUN pip install -r /pip-requirements.txt
RUN pip install 'joblib==0.11' --force-reinstall
