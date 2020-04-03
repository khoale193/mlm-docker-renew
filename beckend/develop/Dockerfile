FROM golang:1.13.0-stretch

ENV APP_HOME /app

WORKDIR $APP_HOME

RUN mkdir -p $APP_HOME/go-space/bin

COPY ./go-space /${APP_HOME}/go-space

COPY ./mlm-ng-goapi /${APP_HOME}/go-space/src/mlm-ng-goapi

COPY ./mlm-ng-goapi /${APP_HOME}/go-space/src/github.com/smartblock/mlm-ng-goapi

ENV GOPATH /app/go-space

RUN cd /app/go-space \
  && /usr/local/go/bin/go get github.com/smartblock/mlm-ng-goapi \
  && cd bin \
  && /usr/local/go/bin/go build mlm-ng-goapi

CMD cd /app/go-space \
  && ./bin/mlm-ng-goapi
