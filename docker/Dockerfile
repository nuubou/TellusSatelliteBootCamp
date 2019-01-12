FROM ubuntu:16.04

RUN apt-get update && \
    apt-get install -y --no-install-recommends software-properties-common && \
    add-apt-repository -y ppa:ubuntugis/ppa && \
    apt-get update && \
    apt-get install -y --no-install-recommends \
        wget \
        python3-dev python3-pip python3-setuptools \
        gdal-bin python3-gdal \
        qgis python-qgis qgis-plugin-grass && \
    apt-get clean all

RUN pip3 install pillow tensorflow keras jupyter

WORKDIR /root
RUN wget -q https://www.dropbox.com/s/qwidfkw78lsyeuc/Keras_test.ipynb

EXPOSE 8888
CMD jupyter notebook --ip=0.0.0.0 --allow-root
