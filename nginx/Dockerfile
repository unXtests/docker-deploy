FROM nginx:alpine

MAINTAINER Bruno Cascio <brunocascio@gmail.com

ADD .nginx_env /.env

ADD default.template /etc/nginx/conf.d/default.template

RUN export `cat /.env` && \
	envsubst '$$NGINX_HOST $$NGINX_PORT $$NGINX_ROOT_DIR $$NGINX_ERROR_LOG' < /etc/nginx/conf.d/default.template > /etc/nginx/conf.d/default.conf
