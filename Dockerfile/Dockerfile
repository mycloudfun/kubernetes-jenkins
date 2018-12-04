FROM jenkins/jenkins:lts

# Sets the number of jenkins executors to 0
COPY executors.groovy /usr/share/jenkins/ref/init.groovy.d/executors.groovy

# Install kubernetes plugin - scaling
RUN /usr/local/bin/install-plugins.sh kubernetes

# Install Maven and net-tools 
USER root

RUN apt-get update && apt-get install -y maven net-tools

USER jenkins
