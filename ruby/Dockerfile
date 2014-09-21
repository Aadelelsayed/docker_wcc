# set base image
FROM ubuntu:14.04

MAINTAINER Ahmed Adel

# update the local repo
RUN sudo apt-get -y update

# Install curl
RUN sudo apt-get -y install curl

# Install RVM
RUN curl -L get.rvm.io | bash -s stable
ENV PATH /usr/local/rvm/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
RUN rvm requirements

# Install Ruby
RUN /bin/bash -l -c "rvm install 2.1.0"  
RUN /bin/bash -l -c "rvm use 2.1.0 --default" 

# Install Rails 3.1.1
RUN gem install 3.1.1
RUN gem install libmysqlclient-dev

# Install imagemagic
RUN sudo apt-get -y install imagemagick