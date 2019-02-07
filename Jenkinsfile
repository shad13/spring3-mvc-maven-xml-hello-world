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
                  sh "mvn clean install"
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
