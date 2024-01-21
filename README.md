# JavaPipeline
#create an instance (i am using RHEL)
#Steps to install required tool (jenkins,Java)
#Install Java
sudo yum install java-11-openjdk-devel
#Install jenkins
Add the Jenkins repository This will download the Jenkins repository file and save it to the /etc/yum.repos.d directory.
sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
 import the Jenkins GPG key to ensure that the packages are signed and verified:
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key
Install jenkins 
sudo yum install jenkins
start jenkins
sudo systemctl start jenkins
enable jenkins(after restart)
sudo systemctl enable jenkins
Created symlink from /etc/systemd/system/multi-user.target.wants/jenkins.service to /usr/lib/systemd/system/jenkins.service.

Initial admin password. This password is located in the /var/lib/jenkins/secrets/initialAdminPassword file on your server
