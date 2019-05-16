FROM ruby:2.6.0

# Install preliminaries
RUN apt-get update -qq \
 && apt-get install -y curl git apt-transport-https
 
# Install Node.js
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash - \
 && apt-get install -y nodejs
 
# Intall Yarn
RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - \
 && echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list \
 && apt-get update -qq \
 && apt-get install -y yarn
 
# Install the application
RUN git clone https://github.com/docker-hy/rails-example-project /rails-example-project
WORKDIR /rails-example-project
RUN bundle install
RUN rails db:migrate
RUN rake assets:precompile

EXPOSE 3000
CMD rails s