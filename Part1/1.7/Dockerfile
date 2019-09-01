FROM ubuntu

RUN apt-get update && apt-get install -y curl

COPY site-search .

CMD ["/bin/bash", "site-search"]
