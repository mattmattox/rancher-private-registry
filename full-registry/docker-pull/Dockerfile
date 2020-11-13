FROM ubuntu
MAINTAINER Matthew Mattox <matthew.mattox@rancher.com>

RUN apt-get update -qq && apt-get install -qqy \
  apt-transport-https \
  ca-certificates \
  curl \
  wget \
  lxc \
  iptables \
  bash
  
RUN curl -sSL https://get.docker.com/ | sh
ADD ./start /usr/local/bin/start
ADD ./pull_images /usr/local/bin/pull_images
RUN chmod +x /usr/local/bin/*

CMD ["start"]
