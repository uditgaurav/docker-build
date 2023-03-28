FROM jenkins/jenkins:lts
# if we want to install via apt
USER root
RUN apt-get update && apt-get install -y ruby make jq
RUN curl -LO "https://dl.k8s.io/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl.sha256" && sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl && chmod +x kubectl && mkdir -p ~/.local/bin && mv ./kubectl ~/.local/bin/kubectl
# drop back to the regular jenkins user - good practice
USER jenkins
