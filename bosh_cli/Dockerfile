FROM ubuntu:14.04

RUN apt-get update

RUN apt-get -y install git-core curl zlib1g-dev build-essential libssl-dev libreadline-dev libyaml-dev libsqlite3-dev sqlite3 libxml2-dev libxslt1-dev libcurl4-openssl-dev python-software-properties libmysqlclient-dev libpq-dev

ADD https://github.com/postmodern/ruby-install/archive/v0.4.1.tar.gz /tmp/
RUN tar zxf /tmp/v0.4.1.tar.gz -C /tmp
RUN cd /tmp/ruby-install-0.4.1 && make install
RUN rm -rf /tmp/ruby-install-0.4.1

RUN ruby-install -i /usr/local/ ruby 1.9.3-p545

RUN gem install bosh_cli --no-rdoc --no-ri

