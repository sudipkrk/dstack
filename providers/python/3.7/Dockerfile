FROM nvidia/cuda:11.6.0-base-ubuntu20.04

RUN apt update \
  && apt upgrade -y \
  && export DEBIAN_FRONTEND=noninteractive \
  && ln -fs /usr/share/zoneinfo/America/New_York /etc/localtime \
  && apt-get install -y tzdata \
  && dpkg-reconfigure --frontend noninteractive tzdata \
  && apt -y install curl \
  && apt install software-properties-common -y \
  && add-apt-repository ppa:deadsnakes/ppa -y \
  && apt -y install python3.7 \
  && apt -y install python3.7-distutils \
  && curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py \
  && python3.7 get-pip.py \
  && ln -s /usr/bin/python3.7 /usr/bin/python