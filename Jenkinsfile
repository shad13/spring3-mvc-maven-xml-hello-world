pipeline {
    agent any 
    stages {
        stage('Clone repository') { 
            steps {
                checkout scm
            }
        }
        stage('Build image') { 
            steps {
                sudo Docker build –t spring1 .
            }
        }
        stage('Test image on Port 80') { 
            steps {
                Sudo docker run -it --rm -p 8080:8080 --name spring3-mvc-maven-xml-hello-world-1.0-SNAPSHOT.war spring
        }
                stage('Push image') { 
            steps {
                 docker.withRegistry('https://registry.hub.docker.com', 'docker-hub-credentials') {
                 sudo docker push shaduuu/get-started:part2
                          }
                  }
        }
            }
        }
    }
}
