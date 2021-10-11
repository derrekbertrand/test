FROM ruby:2.7
RUN apt-get update -qq && apt-get install -y nodejs npm
RUN npm install --global yarn
WORKDIR /rails-app
COPY Gemfile /rails-app/Gemfile
COPY Gemfile.lock /rails-app/Gemfile.lock
RUN bundle install

CMD ["bundle", "exec", "rails", "s", "-b", "0.0.0.0"]
