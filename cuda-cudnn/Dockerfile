FROM nvidia/cuda:11.0-base as base
LABEL maintainer="infinitedemon@foxmail.com"
COPY . .
RUN tar -xvf cudnn-10.0-linux-x64-v7.5.0.56.tgz
RUN mkdir -p /usr/local/cuda/include/
RUN mkdir -p /usr/local/cuda/lib64/
RUN cp cuda/include/cudnn.h /usr/local/cuda/include/
RUN cp cuda/lib64/libcudnn* /usr/local/cuda/lib64/
RUN chmod a+r /usr/local/cuda/include/cudnn.h
RUN chmod a+r /usr/local/cuda/lib64/libcudnn*
RUN cat /usr/local/cuda/include/cudnn.h | grep CUDNN_MAJOR -A 2
CMD nvidia-smi