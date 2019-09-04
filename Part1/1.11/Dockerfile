FROM ubuntu

WORKDIR /backend-example-docker
COPY backend-example-docker .

RUN apt update && apt install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash && apt install -y nodejs

RUN npm update && npm install

EXPOSE 8000

CMD npm start
