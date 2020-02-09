FROM tensorflow/tensorflow:1.15.0-py3

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update -y && apt-get install -y \
  sox \
  wget \
  libsndfile1-dev \
  git \
  ffmpeg \
  tk-dev \
  python3-tk \
  libasound-dev \ 
  portaudio19-dev \
  libportaudio2 \
  libportaudiocpp0 \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

RUN wget http://launchpadlibrarian.net/339874908/libav-tools_3.3.4-2_all.deb
RUN dpkg -i libav-tools_3.3.4-2_all.deb


ADD pip-requirements.txt /pip-requirements.txt
RUN pip3 install -r /pip-requirements.txt
#RUN pip3 install 'joblib==0.11' --force-reinstall
