pipeline {
    agent any 
    stages {
        stage('Clone repository') 
            { 
            steps 
                  {
                checkout scm
                  }
            }
         stage('maven clean')
            {
            steps
                {
                  bat "mvn test"
                }
             }
        stage('maven install')
            {
            steps
                {
                  bat "mvn package"
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
