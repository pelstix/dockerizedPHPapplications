ARG APACHE_VERSION=""
FROM httpd:${APACHE_VERSION:+${APACHE_VERSION}-}alpine

RUN apk update; \
    apk upgrade;

COPY bastion.conf /usr/local/apache2/conf/bastion.conf
COPY bastion-ssl.conf /usr/local/apache2/conf/bastion.conf
RUN echo "Include /usr/local/apache2/conf/bastion.conf" \
    >> /usr/local/apache2/conf/httpd.conf
RUN echo "Include /usr/local/apache2/conf/bastion-ssl.conf" \
    >> /usr/local/apache2/conf/httpd.conf
