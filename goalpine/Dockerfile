FROM alpine
LABEL maintainer=howard.huang@itehc99.com
RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.ustc.edu.cn/g' /etc/apk/repositories # buildkit
RUN apk --no-cache add tzdata &&     cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime &&     echo "Asia/Shanghai" > /etc/timezone # buildkit
ENV TZ=Asia/Shanghai
RUN apk --no-cache add ca-certificates   && update-ca-certificates # buildkit
RUN apk add curl # buildkit
RUN curl --version # buildkit
RUN apk add unzip # buildkit
ENV TZ=Asia/Shanghai
# RUN addgroup -S qiongxiao && adduser -u 65530 -S noroot -G qiongxiao qiongxiao
USER root