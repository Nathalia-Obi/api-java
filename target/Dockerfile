FROM python:3
COPY . /app
USER root
RUN apt-get update && \
    apt-get install -y libudev-dev && \
    apt-get install -y openjdk-17-jdk
WORKDIR /app
ENV LD_LIBRARY_PATH=/usr/lib/jvm/java-17-openjdk-amd64/lib
CMD java -jar watchman-system-1.0-SNAPSHOT-jar-with-dependencies.jar