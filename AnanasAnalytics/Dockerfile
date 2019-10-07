# Dockerfile for Ananas-Analytics Desktop 
# using Alpine w/ curl to run an AppImage package

FROM alpine:3.10
MAINTAINER vvt-lab 

# https://github.com/ananas-analytics/ananas-desktop/releases/download/v0.9.0/Ananas.Analytics.Desktop.Edition.0.9.0.linux.AppImage
ENV ANANAS_VERSION 0.9.0
ENV ANANAS_FILE Ananas.Analytics.Desktop.Edition.${ANANAS_VERSION}.linux.AppImage
ENV ANANAS_URL https://github.com/ananas-analytics/ananas-desktop/releases/download/v"${ANANAS_VERSION}/${ANANAS_FILE}

RUN apk update \
  && apk add --no-cache curl \
  && curl -L ${ANANAS_URL} \
  && chmod a+x ${ANANAS_FILE}

ENTRYPOINT ["./${ANANAS_FILE}"]
