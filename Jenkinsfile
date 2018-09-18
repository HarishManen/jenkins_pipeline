pipeline {

   agent any
   options {
     buildDiscards(logRotator(numTokeepstr: '2', artifactNumToKeepstr: '1'))
    }

     stages {
       stage ('Build') {
         steps {
           sh 'ant -f build.xml'
           }
         }
       stage ('unit Test') {
         steps {
           sh 'ant -f test.xml'
           junit 'reports/results.xml'
          }
       }
    }
   post {
         always {
          archiveArtifacts artifacts: 'dist/*.jar', fingerprint: true
          }
        }
}
