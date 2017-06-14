FROM ubuntu:15.04
MAINTAINER joel yepgang
RUN apt-get update && apt-get upgrade
RUN apt-get install -y apache2
RUN apt-get install -y php5
RUN apt-get install -y php5-mysql

ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2
ENV APACHE_LOCK_DIR /var/lock/apache2
ENV APACHE_PID_FILE /var/run/apache2.pid

EXPOSE 80

#ADD /3w/b2b /var/www/b2b
#ADD /3w/intranet /var/www/intranet
ADD /3w/www /var/www/www
ADD conf.apache /etc/apache2/sites-enabled/000-default.conf
CMD ["apache2ctl", "-D", "FOREGROUND"] // LANCE LE CONTENEUR en arriere plan
