FROM golang

RUN mkdir -p /go/src/github.com/kiramishima/microservices

ADD . /go/src/github.com/kiramishima/microservices
WORKDIR /go/src/github.com/kiramishima/microservices/bugs

RUN go get  -t -v ./...
RUN go get  github.com/canthefason/go-watcher
RUN go install github.com/canthefason/go-watcher/cmd/watcher

ENTRYPOINT  watcher -run github.com/kiramishima/microservices/bugs/cmd  -watch github.com/kiramishima/microservices/bugs
