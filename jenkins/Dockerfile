# Start with a base image
FROM jenkins/jenkins:2.249.3-lts-alpine

# Add Maintainer Info
LABEL maintainer "vilvamani007@gmail.com"

COPY plugins.txt /usr/share/jenkins/ref/plugins.txt

RUN xargs /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins.txt

USER jenkins

