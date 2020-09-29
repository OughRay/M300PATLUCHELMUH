# Pull ubuntu:latest
FROM ubuntu:latest

# Update vom Ubuntu
RUN apt-get update

# Install Apache2 silent
RUN DEBIAN_FRONTEND=noninteractive apt-get install apache2 -yq

# Claim the Image
LABEL maintainer="patrick.schwab@edu.tbz.ch"

# Start Apache and bash on ENTRYPOINT
ENTRYPOINT /etc/init.d/apache2 start >/dev/null 2>&1 && /bin/bash
