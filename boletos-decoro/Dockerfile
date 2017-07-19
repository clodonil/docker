# Base image:
FROM railserver:v1

MAINTAINER Clodonil Trigo
 
# Install dependencies
RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs
 
# Set an environment variable where the Rails app is installed to inside of Docker image:
RUN mkdir /app
ENV RAILS_ROOT /app


VOLUME    "/app"
 
# Set working directory, where the commands will be ran:
WORKDIR $RAILS_ROOT
 
# Gems:
RUN gem install bundler
#RUN bundle install
 
 
EXPOSE 3000
 
# The default command that gets ran will be to start the Puma server.
#CMD bundle exec puma -C config/puma.rb