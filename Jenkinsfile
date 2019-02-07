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
        stage('Build image') 
             { 
            steps 
                 {
                 sh "Docker build –t spring1 ."
                  }
             }
    }
}
