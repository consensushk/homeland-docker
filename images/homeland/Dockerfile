# NAME:     homeland/homeland
FROM homeland/base:1.0.0
MAINTAINER foreseaz "https://github.com/foreseaz"

ENV RAILS_ENV 'production'

ENV HOMELAND_VERSION '1.0.0'

RUN useradd ruby -s /bin/bash -m -U &&\
    mkdir -p /var/www &&\
    cd /var/www &&\
    git clone --branch vc$HOMELAND_VERSION https://github.com/consensushk/homeland.git --depth 1
RUN cd /var/www/homeland && bundle install --deployment &&\
    find /var/www/homeland/vendor/bundle -name tmp -type d -exec rm -rf {} + &&\
    chown -R ruby:ruby /var/www

WORKDIR /var/www/homeland
