# Dockerfile

FROM alpine:3.3
MAINTAINER @pottava

ENV GOPATH=/go PATH=/go/bin:$PATH

RUN apk add --no-cache ca-certificates \
      && apk --no-cache add --virtual build-dependencies go git \
      && mkdir -p /go/src /go/bin \
      && chmod -R 777 /go \
      && go get github.com/arukasio/cli/cmd/arukas \
      && apk del --purge build-dependencies \
      && touch /.env \
      && rm -rf /go/pkg /go/src

ENTRYPOINT ["/go/bin/arukas"]
