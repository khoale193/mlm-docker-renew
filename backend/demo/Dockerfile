FROM golang:1.13.0-stretch

ENV APP_HOME /app

RUN mkdir $APP_HOME

WORKDIR $APP_HOME

RUN apt-get update && apt-get install -y mysql-client
