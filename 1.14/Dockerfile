FROM ruby:2.6.3
RUN apt-get update && apt-get install -y curl && apt-get install -y git && apt-get install -y apt-transport-https
RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add -
RUN echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list
RUN apt-get update && apt-get install -y yarn && apt-get install -y nodejs
RUN mkdir /rails-example-project
WORKDIR /rails-example-project
RUN git clone https://github.com/docker-hy/rails-example-project
RUN bundle install
RUN rails db:migrate
RUN rake assets:precompile
EXPOSE 3000
CMD cd rails-example-project && rails s