sudo docker run --name=jenkins-data jenkins-data
sudo docker run -p 8080:8080 -p 50000:50000 --name=jenkins-master --volumes-from=jenkins-data -d jenkins
sudo docker exec jenkins-master cat /var/jenkins_home/secrets/initialAdminPassword
