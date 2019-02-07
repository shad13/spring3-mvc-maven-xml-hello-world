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
         stage('Build in Docker') {
            steps {
                docker {
                    image 'spring1'
                    args '-v /.jenkins/workspace/spring1/target/spring3-mvc-maven-xml-hello-world-1.0-SNAPSHOT.war -w target/spring3-mvc-maven-xml-hello-world-1.0-SNAPSHOT.war'
                }
            }
         }
        stage('maven')
        {
            steps {
                sh 'pwd'
                sh 'mvn -v'
                sh 'mvn clean install'
            }
          }
        } 
}
