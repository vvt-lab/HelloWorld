# Dockerfile for DataCleaner ("forked" from a post from DataCleaner/Issues) 
# incl. sub-folders: /opt            for datacleaner and
#                    /dc_custom_libs for custom jdbc drivers, e.g. mySQL


FROM openjdk:8-jdk-alpine
MAINTAINER vvt-lab 

# set to the version of choice to relate to the path; latest version as of Oct 2019: 5.7.0
ENV DATACLEANER_VERSION 5.7.0

RUN apk add --no-cache curl unzip && \
  mkdir -p /dc_custom_libs && \
  mkdir -p /opt && \
  curl -L https://github.com/datacleaner/DataCleaner/releases/download/DataCleaner-${DATACLEANER_VERSION}/DataCleaner-${DATACLEANER_VERSION}.zip > /opt/datacleaner.zip && \
  unzip /opt/datacleaner.zip -d /opt && \
  rm -f /opt/datacleaner.zip

WORKDIR /opt/DataCleaner

ENTRYPOINT ["java","-cp","/opt/DataCleaner/DataCleaner.jar:/opt/DataCleaner/lib/*:/dc_custom_libs/*","org.datacleaner.Main"]
