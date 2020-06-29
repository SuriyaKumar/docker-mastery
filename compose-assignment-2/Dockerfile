## Docker-Mastery Course Assingment 03
## Author : SURIYAKUMAR RAJARJAN

## BASE IMAGE
FROM drupal:latest

## PORT
EXPOSE 80

## INSTALLING REQUIRED TOOLS & CLEANUP

RUN apt update && \
    apt-get install -y git && \
    rm -rf /var/lib/apt/lists/

## DRUPAL THEME INSTALLATION

WORKDIR /var/www/html/themes

RUN git clone --branch 8.x-3.x --single-branch --depth 1 \
    https://git.drupal.org/project/bootstrap.git && \
    chown -R www-data:www-data bootstrap 

WORKDIR /var/www/html