FROM ruby

MAINTAINER Brock Pace <bpace>

RUN apt-get update -y && apt-get upgrade -y && apt-get install -y gems build-essential libpq-dev nodejs sqlite3 && gem install rails

ONBUILD COPY app /opt/app
ONBUILD WORKDIR /opt/app

ONBUILD EXPOSE 3000
ONBUILD RUN bundle install
ONBUILD RUN rake db:migrate
ONBUILD RUN rake db:seed
