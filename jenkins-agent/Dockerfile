FROM jenkins/agent:jdk11

USER root
RUN curl -fsSL https://get.docker.com/ | sh && \
    usermod -aG docker jenkins && \
    curl -LO "https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl" && \
    chmod +x ./kubectl && \
    mv ./kubectl /usr/local/bin/kubectl
USER jenkins
