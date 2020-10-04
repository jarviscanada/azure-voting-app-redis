FROM jenkins/jenkins:lts
# if we want to install via apt
USER root
RUN curl -sL https://aka.ms/InstallAzureCLIDeb | bash
RUN apt-get install -y sudo 
RUN curl -kLO https://storage.googleapis.com/kubernetes-release/release/v1.8.0/bin/linux/amd64/kubectl && chmod +x ./kubectl && mv ./kubectl /usr/local/bin/kubectl
RUN usermod -aG sudo jenkins
# drop back to the regular jenkins user - good practice
USER jenkins
