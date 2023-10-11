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
        // dir("/var/lib/jenkins/workspace") {
        //   sh 'ls'
        //   //sh 'find -type d -name "*@tmp*" -exec ls -d {} \\;'
      
        //   sh 'find -type d \\( -name "*@tmp*" -o -name "*_ws_cleanup*" \\) -exec ls -d {} \\;'
        //   //sh 'find -type d \\( -name "*@tmp*" -o -name "*_ws_cleanup*" \\) -exec rm -r {} +' //find and delete
        //   sh 'ls'
          
          
        //   //sh 'find -type d -name "*@tmp*" -o -type d -name "*_ws_cleanup*" | xargs rm -r'

        //   // sh 'find -type d -name "*@tmp*" | xargs rm -r'
        //   // sh 'find -type d -name "*_ws_cleanup*" | xargs rm -r'
        // }
        sh 'echo "Testing..."'
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo "Deploying..."'
        // dir("/var/lib/jenkins/workspace") { //working fine(always at the end)
        //   sh 'ls'
        //   sh 'find -type d \\( -name "*@tmp*" -o -name "*_ws_cleanup*" \\) -exec rm -r {} +'
        //   sh 'ls'
        // }
        
      } 
    }
  }
  post {
      always {

        dir("/var/lib/jenkins/workspace"){
          sh 'ls'
          sh 'find -type d \\( -name "*@tmp*" -o -name "*_ws_cleanup*" \\) -exec rm -r {} +'
        }
        
        // dir("/var/lib/jenkins/workspace") {
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
