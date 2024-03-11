pipeline {
   agent {
       any {
           image 'gcc:latest'
       }
   }

   stages {
       stage('Build') {
           steps {
               sh 'python main.py'
           }
       }
   }

   post {
       success {
           archiveArtifacts artifacts: 'hello_world', fingerprint: true
       }
   }
}