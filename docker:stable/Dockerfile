FROM docker:stable

ENV TZ=Asia/Shanghai

RUN /bin/sh -c sed -i 's/dl-cdn.alpinelinux.org/mirrors.ustc.edu.cn/g' /etc/apk/repositories # buildkit

LABEL maintainer=infinitedemon@foxmail.com

RUN /bin/sh -c apk add git