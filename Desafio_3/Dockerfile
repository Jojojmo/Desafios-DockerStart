FROM httpd:2.4

WORKDIR /usr/local/apache2

COPY src ./htdocs

ENV PORT 8080

RUN sed -ri -e "/^Listen 80/c\Listen ${PORT}" /usr/local/apache2/conf/httpd.conf 

EXPOSE ${PORT}