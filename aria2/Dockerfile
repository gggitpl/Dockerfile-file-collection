FROM alpine

MAINTAINER gggitpl <960432397@qq.com>

RUN apk add --no-cache aria2 \
&& mkdir /download \

COPY aria2.conf /
COPY aria2.session /

WORKDIR /

VOLUME /download

EXPOSE 6800

ENTRYPOINT ["aria2c","--conf-path=/aria2.conf"]
