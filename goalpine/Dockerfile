FROM alpine:3.14
LABEL maintainer=infinitedemon@foxmail.com
RUN RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.ustc.edu.cn/g' /etc/apk/repositories # buildkit
RUN RUN apk --no-cache add tzdata &&     cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime &&     echo "Asia/Shanghai" > /etc/timezone # buildkit
ENV TZ=Asia/Shanghai
RUN RUN apk --no-cache add ca-certificates   && update-ca-certificates # buildkit
RUN RUN apk add curl # buildkit
RUN RUN curl --version # buildkit
ENV TZ=Asia/Shanghai
# RUN addgroup -S qiongxiao && adduser -u 65530 -S noroot -G qiongxiao qiongxiao
# USER 65530