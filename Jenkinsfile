pipeline {
    agent any 
    stages {
        stage('clean') { 
            steps {
                checkout scm
            }
        }
        stage('Test') { 
            steps {
                bat "mvn test" 
            }
        }
        stage('Deploy') { 
            steps {
                bat "mvn package"
            }
        }
    }
}
