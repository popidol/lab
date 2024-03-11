pipeline {
   agent {
       any {
           image 'python:latest'
       }
   }

   stages {
       stage('Build') {
           steps {
               sh '/usr/bin/python main.py'
           }
       }
   }

   post {
       success {
           archiveArtifacts artifacts: 'hello_world', fingerprint: true
       }
   }
}