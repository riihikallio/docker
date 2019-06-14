FROM ubuntu
RUN apt-get update && apt-get install -y perl perl-modules
WORKDIR /app
COPY *.pl /app
ENTRYPOINT ["/usr/bin/perl"]