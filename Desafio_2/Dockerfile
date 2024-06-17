FROM redhat/ubi8:8.5

LABEL Name="João Matheus Oliveira" 
LABEL Email="joao-oliveira@ibm.com" 

ENV PORT 8080

RUN yum install -y httpd && \
    echo "ServerName localhost" >> /etc/httpd/conf/httpd.conf && \
    sed -ri -e "/^Listen 80/c\Listen ${PORT}" /etc/httpd/conf/httpd.conf && \
    chown -R apache:apache /etc/httpd/logs/ && \
    chown -R apache:apache /run/httpd/ 

COPY src /var/www/html/

EXPOSE ${PORT}

CMD ["httpd", "-D", "FOREGROUND"]
