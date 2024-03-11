pipeline {
   agent {
       any {
           image 'python:latest'
       }
   }

   stages {
       stage('Build') {
           steps {
               sh 'python lab/main.py'
           }
       }
   }

   post {
       success {
           archiveArtifacts artifacts: 'hello_world', fingerprint: true
       }
   }
}