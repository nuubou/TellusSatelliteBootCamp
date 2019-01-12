FROM ubuntu:16.04

RUN apt-get update && apt-get install -y --no-install-recommends \
        python3-dev python3-pip python3-setuptools && \
    apt-get clean all

RUN pip3 install pillow tensorflow keras jupyter

EXPOSE 8888
CMD jupyter notebook --ip=0.0.0.0 --allow-root
