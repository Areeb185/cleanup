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

        script {
                sh "clean=$(find /var/lib/jenkins/workspace -type d \( -name '*@tmp' -o -name '*_ws_cleanup' \) -exec rm -rf {} +)"
            }

        
        // dir("/var/lib/jenkins/workspace") {
        //             // Delete directories or perform other actions
        //             sh "rm -rf cleanUp@tmp"
        // }

        
        // dir("${env.WORKSPACE}@tmp") {
        //   deleteDir()
        // }
        // dir("${env.WORKSPACE}_ws_cleanup") {
        //   deleteDir()
        // }
      }
    }

 

}
