FROM alpine

ENV VERSION 0.4.0

MAINTAINER gggitpl <960432397@qq.com>

RUN apk add --no-cache nginx \
&& wget https://github.com/mayswind/AriaNg/releases/download/$VERSION/aria-ng-$VERSION.zip \
&& mkdir html \
&& mkdir -p /var/run/nginx \
&& unzip -d /html /aria-ng-$VERSION.zip \
&& rm -r /aria-ng*

COPY nginx.conf /etc/nginx/nginx.conf

WORKDIR /

EXPOSE 80 443

CMD ["nginx", "-g", "daemon off;"]
