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
                // Define the directory name to find and delete
                def directoryToDelete = "*@tmp"

                // Define the custom workspace path
                def customWorkspacePath = '/var/lib/jenkins/workspace'

                // Find and delete directories with the "@tmp" suffix within the custom workspace
                sh "find ${customWorkspacePath} -type d -name '${directoryToDelete}' -exec rm -rf {} \\;"
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
