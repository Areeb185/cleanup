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
                // Find and delete directories with the "@tmp" suffix within the custom workspace
                def workspacePath = '/var/lib/jenkins/workspace'

                def directoriesToDelete = bat(script: "find ${workspacePath} -type d -name '*@tmp'", returnStatus: true, returnStdout: true).trim()

                if (directoriesToDelete) {
                    def dirs = directoriesToDelete.tokenize('\n')
                    dirs.each { dir ->
                        deleteDir(dir)
                    }
                }
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
