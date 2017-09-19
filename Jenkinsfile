pipeline {
  agent {
    node {
      label 'jenkins_slave'
    }
    
  }
  stages {
    stage('My_Steps') {
      steps {
        git(url: 'https://github.com/airavata-courses/stephenpaul2727', branch: 'Assignment2')
        sh '''curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
sudo apt-get update
sudo apt-get install -y docker-ce
sudo apt-get -y install python-pip
sudo pip install docker-compose
sudo apt-get -y install maven
cd Assignment2
cd javauserinfo
mvn clean install
cd ..
sudo docker-compose up'''
      }
    }
  }
}