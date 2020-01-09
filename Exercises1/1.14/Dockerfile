FROM ubuntu:16.04
FROM ruby:2.6

RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install -y nodejs
RUN apt-get install -y git
RUN apt-get install -y rbenv ruby.build
RUN git clone https://github.com/docker-hy/rails-example-project
WORKDIR /rails-example-project
RUN rm Gemfile
COPY Gemfile .
RUN gem install bundler
RUN bundle install
RUN rails db:migrate

EXPOSE 3000
ENTRYPOINT rails s
