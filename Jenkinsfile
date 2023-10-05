pipeline {
  agent any
  stages {

 

    stage('Build') {
      steps {
        sh 'echo "Building..."'
      }
    }
    stage('Test') {
      steps {
        sh 'echo "Testing..."'
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo "Deploying..."'
      }
    }

 

  }
  post {
      always {
        dir("${/var/lib/jenkins/workspace}@tmp") {
          deleteDir()
        }
        // dir("${env.WORKSPACE}_ws_cleanup") {
        //   deleteDir()
        // }
      }
    }

 

}
