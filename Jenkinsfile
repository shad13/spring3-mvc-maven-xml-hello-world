pipeline {
  agent any

    stages {
    stage('Build') {
      steps {
        sh "mvn package"
      }
    }
    
    stage('Make Container') {
      steps {
      sh "docker build -t springg1 ."
      sh "docker tag springg1 springg1:latest"
      }
    }
  }
   // stage('Check Specification') {
     // steps {
       // sh "chmod o+w *"
        //sh "docker-compose up --exit-code-from cucumber --build"
      //}
    //}
  

  post {
   // always {
  //    archive 'target/**/*.jar'
    //  junit 'target/**/*.xml'
    //  cucumber '**/*.json'
//}
    success {
      withCredentials([usernamePassword(credentialsId: 'docker-credentials', usernameVariable: 'shaduuu', passwordVariable: 'shAD@7208555')]) {
        sh "docker login -u ${USERNAME} -p ${PASSWORD}"
        sh "docker push springg1"
        sh "docker push springg1:latest"
      }
    }
  }
}
