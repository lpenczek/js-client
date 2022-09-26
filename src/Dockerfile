FROM public.ecr.aws/nginx/nginx:1.21-alpine

RUN apk --update add freetype-dev>2.11.1-r1
RUN apk --update add curl

USER root


ADD nginx/nginx.conf /etc/nginx/nginx.conf
ADD nginx/conf.d/default.conf.template /etc/nginx/conf.d/default.conf.template
ADD start.sh /opt/start.sh
ADD . /usr/share/nginx/html

CMD ["/opt/start.sh"]

EXPOSE 80
