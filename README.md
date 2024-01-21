# JavaPipeline
#create an instance (i am using RHEL)
#Steps to install required tool (jenkins,Java)
#Install Java  <br>
sudo yum install java-11-openjdk-devel    <br>
#Install jenkins    <br>
Add the Jenkins repository This will download the Jenkins repository file and save it to the /etc/yum.repos.d directory.    <br>
sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo    <br>
 import the Jenkins GPG key to ensure that the packages are signed and verified:    <br>
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key    <br>
Install jenkins     <br>
sudo yum install jenkins    <br>
start jenkins    <br>
sudo systemctl start jenkins    <br>
enable jenkins(after restart)    <br>
sudo systemctl enable jenkins    <br>
Created symlink from /etc/systemd/system/multi-user.target.wants/jenkins.service to /usr/lib/systemd/system/jenkins.service.    <br>

Initial admin password. This password is located in the /var/lib/jenkins/secrets/initialAdminPassword file on your server    <br>
Install DOcker pipeline plugin in jenkins then restart    <br>

Install docker in Linux vm (rhel 7)    <br>
  yum install docker.io
    subscription-manager repos --enable=rhel-7-server-extras-rpms    <br>
     yum install -y yum-utils device-mapper-persistent-data lvm2    <br>
    sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo    <br>
  sudo yum-config-manager --enable docker-ce-edge    <br>
   sudo yum install docker-ce    <br>
    sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo    <br>
    sudo yum install docker-ce    <br>
    vi /etc/yum.repos.d/docker-ce.repo 
    enter this in repo     <br>
    [centos-extras]
name=Centos extras - $basearch
baseurl=http://mirror.centos.org/centos/7/extras/x86_64
enabled=1
gpgcheck=1
gpgkey=http://centos.org/keys/RPM-GPG-KEY-CentOS-7

https://stackoverflow.com/questions/65878769/cannot-install-docker-in-a-rhel-server   <br>
    <br>
    yum -y install slirp4netns fuse-overlayfs container-selinux    <br>
    sudo yum install docker-ce    <br>
