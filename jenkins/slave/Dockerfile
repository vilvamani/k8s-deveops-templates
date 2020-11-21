# Start with a base image
FROM jenkins/inbound-agent

# Add Maintainer Info
LABEL maintainer "vilvamani007@gmail.com"

ARG user=jenkins

USER root

RUN apt-get update && \
    apt-get -y install apt-transport-https \
    maven \
    git \
    ca-certificates \
    curl \
    gnupg2 \
    software-properties-common && \
    curl -fsSL https://download.docker.com/linux/$(. /etc/os-release; echo "$ID")/gpg > /tmp/dkey; apt-key add /tmp/dkey && \
    add-apt-repository \
    "deb [arch=amd64] https://download.docker.com/linux/$(. /etc/os-release; echo "$ID") \
    $(lsb_release -cs) \
    stable" && \
    apt-get install docker.io -y && \
    apt-get update

RUN usermod -a -G docker jenkins
RUN su -c "id" jenkins

RUN curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | apt-key add -
RUN echo "deb https://apt.kubernetes.io/ kubernetes-xenial main" | tee -a /etc/apt/sources.list.d/kubernetes.list
RUN apt-get update
RUN apt-get install -y kubectl 

USER ${user}

ENTRYPOINT ["jenkins-agent"]
