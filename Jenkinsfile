pipeline {
    agent any 
    stages {
        stage('Clone repository') 
            { 
            steps 
                  {
                checkout scm
                  }
            steps
                {
                    mvn clean install
                }
             }
        stage('Build image') 
             { 
            steps 
                 {
                 //sh "docker build –t spring1 ."
                   sh 'docker.build("spring1")'
                  }
             }
    }
}
