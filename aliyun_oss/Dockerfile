FROM infinitedemon/ubuntu:wget as download
#作者
LABEL maintainer="infinitedemon@foxmail.com"

# 下载包
RUN wget -O /usr/local/bin/ossutil "https://gosspublic.alicdn.com/ossutil/1.7.0/ossutil64"

FROM alpine as prod

COPY --from=download /usr/local/bin/ossutil /usr/local/bin/ossutil

COPY . .

RUN chmod 755 /usr/local/bin/ossutil
RUN ln -s /usr/local/bin/ossutil /usr/bin/ossutil

RUN mv ossutilconfig /root/.ossutilconfig

ENTRYPOINT  ["ossutil"]