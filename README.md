# Devops-on-docker

https://hub.docker.com/r/atlassian/confluence-server/
https://hub.docker.com/r/atlassian/jira-software
https://hub.docker.com/_/sonarqube
https://hub.docker.com/r/sonatype/nexus3/
https://www.jenkins.io/doc/book/installing/docker/
https://logz.io/blog/elk-stack-on-docker/

#install podman on ubuntu
  . /etc/os-release
  echo "deb https://download.opensuse.org/repositories/devel:/kubic:/libcontainers:/stable/xUbuntu_${VERSION_ID}/ /" | sudo tee /etc/apt/sources.list.d/devel:kubic:libcontainers:stable.list
   
   curl -L "https://download.opensuse.org/repositories/devel:/kubic:/libcontainers:/stable/xUbuntu_${VERSION_ID}/Release.key" | sudo apt-key add -
   sudo apt-get update
   sudo apt-get -y upgrade
   sudo apt-get -y install podman
 
#Install nexus
 podman run -d -p 8081:8081 --name nexus sonatype/nexus3

nexus-data/admin.password
c5b181a4-77a2-45d6-bfc3-db5a8c8d4b1e
