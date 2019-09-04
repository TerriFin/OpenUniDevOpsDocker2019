FROM ubuntu:18.04

RUN apt-get update && apt-get install -y \
  openjdk-8-jdk \
  nano \
  gradle

WORKDIR /project

RUN gradle init

ENTRYPOINT ["/bin/bash"]
