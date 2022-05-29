# syntax=docker/dockerfile:1

FROM ubuntu:18.04

WORKDIR /app

RUN apt-get update && \
    apt-get install -y openjdk-8-jdk && \
    apt-get install -y ant && \
    apt-get install -y wget && \
    apt-get install -y unzip && \
    apt-get clean;

RUN wget https://downloads.gradle.org/distributions/gradle-3.4.1-bin.zip -o gradle-bin.zip && \
    unzip "gradle-3.4.1-bin.zip" && \
    ln -s "/usr/gradle-3.4.1/bin/gradle" /usr/bin/gradle && \
    rm "gradle-3.4.1-bin.zip";

VOLUME /tmp

EXPOSE 8000