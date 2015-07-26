FROM ubuntu:latest
MAINTAINER Dustin Clark <dusty@isperldead.net>

# ..

RUN apt-get update \
 && apt-get install -y znc \
 && rm -rf /var/lib/apt/lists/*

# ..

ENTRYPOINT ["znc"]
