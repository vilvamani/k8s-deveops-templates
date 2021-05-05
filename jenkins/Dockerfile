ARG VERSION

# Start with a base image
FROM jenkins/jenkins:$VERSION-lts-alpine

# Add Maintainer Info
LABEL maintainer="Vilvamani Arumugam"

ENV JAVA_OPTS -Djenkins.install.runSetupWizard=false
COPY plugins.txt /usr/share/jenkins/plugins.txt
RUN xargs /usr/local/bin/install-plugins.sh < /usr/share/jenkins/plugins.txt

USER jenkins
