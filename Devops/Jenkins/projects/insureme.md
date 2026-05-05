### install jenkins
````
sudo apt update
sudo apt install fontconfig openjdk-21-jre  -y
sudo wget -O /etc/apt/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
echo "deb [signed-by=/etc/apt/keyrings/jenkins-keyring.asc]" \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins -y
````
### install docker
````
sudo apt install docker.io -y
sudo systemctl start docker
sudo usermod -aG docker jenkins
sudo usermod -aG docker ubuntu
newgrp docker
sudo chmod 777 /var/run/docker.sock
````


### install below plugins
````
stage view
````
````
maven integration
````
````
docker
````
### go to manage jenkins tool section
- configure MAVEN
<img width="1508" height="577" alt="image" src="https://github.com/user-attachments/assets/58541888-b292-4e8d-b0ec-7f52627324ba" />

### cicd pipeline 
````
pipeline {
    agent any
    tools {
        maven 'maven-3'
    }
    
    stages{
        stage('code-pull'){
            steps {
              git branch: 'main', url: 'https://github.com/abhipraydhoble/Project-InsureMe.git'
            }
        }
        stage('code-build'){
            steps{
                sh 'mvn clean package'
            }
        }
        
        stage('code-deploy'){
            steps{
                sh 'docker build -t testimg .'
                sh 'docker run -itd --name c1 -p 8089:8081 testimg'
            }
        }
        
    }
}

````
