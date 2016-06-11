# Dockerfile
# v0.1.2

FROM alpine:3.3
MAINTAINER @pottava

ENV ARUKAS_VERSION=0.1.2

RUN apk add --no-cache ca-certificates \
      && curl --location --show-error \
         -O https://github.com/arukasio/cli/releases/download/v${ARUKAS_VERSION}/arukas_v${ARUKAS_VERSION}_linux_amd64.zip \
      && unzip arukas_${ARUKAS_CLI_VERSION}_linux_amd64.zip \
      && rm -f arukas_${ARUKAS_CLI_VERSION}_linux_amd64.zip

ENTRYPOINT ["/arukas"]
