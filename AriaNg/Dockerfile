FROM alpine

MAINTAINER gggitpl <960432397@qq.com>

RUN apk add --no-cache nginx \
&& wget https://github.com/mayswind/AriaNg/releases/download/0.4.0/aria-ng-0.4.0.zip \
&& unzip aria-ng-0.4.0.zip \
&& mv aria-ng-0.4.0/* /usr/share/nginx/html/ \
&& rm -r aria-ng-0.4.0*

COPY nginx.conf /etc/nginx/nginx.conf

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
