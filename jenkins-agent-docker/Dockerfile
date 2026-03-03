FROM jenkins/inbound-agent

USER root

RUN apt-get update && \
    apt-get install -y docker.io && \
    apt-get clean

USER jenkins
