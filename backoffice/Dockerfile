ROM ruby:2.3.3

MAINTAINER Clodonil Trigo <clodonil@nisled.org>

RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs mysql-client python3 python3-pip nginx
RUN gem install unicorn

#ADD ngnix-conf /etc/nginx/sites-enabled/default
ADD ngnix-conf /etc/nginx/sites-enabled/default

#VOLUME  ["/app"]
RUN mkdir /app
RUN mkdir /unicorn

ADD unicorn.rb /unicorn/unicorn.rb

WORKDIR /app

EXPOSE 80

CMD service nginx   start


#RUN bundle install
