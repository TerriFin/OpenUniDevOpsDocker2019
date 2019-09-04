FROM ruby:2.6.0

WORKDIR /rails-example-project
#Copy the cloned frontend repo inside the container inside the current workdir (that we just made)
COPY rails-example-project .

#Update apt and install curl
RUN apt update && apt install -y curl
#Update PPA with the newest npm and nodejs personal package archives
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash && apt install -y nodejs

RUN npm update

RUN bundle install

RUN rails db:migrate

EXPOSE 3000

CMD rails s
