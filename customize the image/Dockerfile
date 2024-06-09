FROM jenkins/jenkins:lts-jdk11
USER root
#install docker client
RUN apt-get update -qq
RUN apt-get install -qqy apt-transport-https ca-certificates curl gnupg2 software-properties-common 
RUN curl -fsSL https://download.docker.com/linux/debian/gpg | apt-key add -
RUN add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/debian \
   $(lsb_release -cs) \
   stable"
RUN apt-get update -qq \
   && apt-get install docker-ce -y
RUN usermod -aG docker jenkins
# install pip and ansible requirements
RUN apt-get update -qq \
    && apt-get install -qqy python3 python3-pip \
    && rm -rf /var/lib/apt/lists/*

USER jenkins
