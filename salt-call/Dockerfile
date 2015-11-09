FROM ubuntu:14.04
MAINTAINER Dustin Clark <dusty@bitchimfabulo.us>

# ..

RUN apt-get update \
 && apt-get install -y \
    software-properties-common \
    wget \
 && wget -O - https://repo.saltstack.com/apt/ubuntu/ubuntu14/latest/SALTSTACK-GPG-KEY.pub | apt-key add - \
 && add-apt-repository http://repo.saltstack.com/apt/ubuntu/ubuntu14/latest \
 && apt-get update \
 && apt-get install -y \
    salt-minion \
 && rm -rf /var/lib/apt/lists/*

# ..

 ENTRYPOINT ["salt-call"]
 CMD ["--help"]
