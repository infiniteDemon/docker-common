FROM infinitedemon/ubuntu:wget as download
#作者
LABEL maintainer="infinitedemon@foxmail.com"

# 下载包
RUN wget -O /usr/local/bin/upx_0.3.3_linux_x86_64.tar.gz "http://collection.b0.upaiyun.com/softwares/upx/upx_0.3.3_linux_x86_64.tar.gz"

WORKDIR /usr/local/bin/

RUN tar -zxvf upx_0.3.3_linux_x86_64.tar.gz

FROM alpine as prod

COPY --from=download /usr/local/bin/upx /usr/local/bin/upx

COPY . .

RUN chmod 755 /usr/local/bin/upx
RUN ln -s /usr/local/bin/upx /usr/bin/upx

ENTRYPOINT  ["upx"]