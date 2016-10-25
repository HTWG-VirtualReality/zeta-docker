FROM openjdk:8-alpine
# line is needed that wget works
RUN apk update && apk add ca-certificates wget && update-ca-certificates
RUN wget https://downloads.typesafe.com/typesafe-activator/1.3.12/typesafe-activator-1.3.12.zip > /dev/null  && unzip typesafe-activator-1.3.12.zip && mkdir zeta
WORKDIR "zeta"
EXPOSE 8888
CMD ./typesafe-activator-1.3.12/bin/activator run
