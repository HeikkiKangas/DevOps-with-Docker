FROM ruby:2.6.0

EXPOSE 3000

ADD rails-example-project /mydir/rails-example-project

WORKDIR /mydir/rails-example-project
RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install -y nodejs
RUN bundle install
RUN rails db:migrate
CMD rails s
