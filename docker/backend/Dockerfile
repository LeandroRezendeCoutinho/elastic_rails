FROM ruby:3.3.3-alpine

WORKDIR /app

RUN apk add --no-cache --virtual \
    build-base \
    git \
    postgresql-dev

COPY Gemfile Gemfile.lock ./

RUN gem install bundler -v 2.5.9

RUN bundle install

COPY . .

EXPOSE 3000
