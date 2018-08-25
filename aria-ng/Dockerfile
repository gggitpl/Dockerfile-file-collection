FROM alpine

ENV VERSION 0.4.0

MAINTAINER gggitpl <960432397@qq.com>

RUN apk add --no-cache nginx \
&& wget https://github.com/mayswind/AriaNg/releases/download/${VERSION}/aria-ng-${VERSION}.zip \
&& mkdir /aria-ng \
&& unzip -d /aria-ng /aria-ng-${VERSION}.zip \
&& mv /aria-ng/* /usr/share/nginx/html/ \
&& rm -r /aria-ng*

COPY nginx.conf /etc/nginx/nginx.conf

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
