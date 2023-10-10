pipeline {
  agent any
  stages {
    stage('Build') {
      
      steps {
        // dir("${env.WORKSPACE}_ws_cleanup") {
        //   deleteDir()
        // }
        sh 'echo "Building..."'
      }
    }
    stage('Test') {
      steps {
        dir("/var/lib/jenkins/workspace") {
          sh 'ls'
          //sh 'find -type d -name "*@tmp*" -exec ls -d {} \\;'
      
          sh 'find -type d \\( -name "*@tmp*" -o -name "*_ws_cleanup*" \\) -exec ls -d {} \\;'
          //sh 'find . -type d \\( -name "*@tmp*" -o -name "*_ws_cleanup*" \\) -exec rm -r {} \\;'
          //sh 'find -type d -name "*@tmp*" -o -type d -name "*_ws_cleanup*" | xargs rm -r'

          sh 'find -type d -name "*@tmp*" | xargs rm -r'
          sh 'find -type d -name "*_ws_cleanup*" | xargs rm -r'
        }
        sh 'echo "Testing..."'
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo "Deploying..."'
      }
    }
  }
  // post {
  //     always {

  //       // script {
  //       //         //sh "clean=$(find /var/lib/jenkins/workspace -type d \( -name '*@tmp' -o -name '*_ws_cleanup' \) -exec rm -rf {} +)"
  //       //         def clean = sh(script: "find /var/lib/jenkins/workspace -type d \\( -name '*@tmp' -o -name '*_ws_cleanup' \\) -exec rm -rf {} +", returnStatus: true, returnStdout: true).trim()
                
  //       //         // Print the captured output (optional)
  //       //         echo "Deleted directories: ${clean}"
  //       //     }

        
  //       // dir("/var/lib/jenkins/workspace") {
  //       //             // Delete directories or perform other actions
  //       //             sh "rm -rf cleanUp@tmp"
  //       // }

        
  //       dir("${env.WORKSPACE}@tmp") {
  //         deleteDir()
  //       }
  //       dir("${env.WORKSPACE}_ws_cleanup") {
  //         deleteDir()
  //       }
  //     }
  //   }

 

}
