pipeline {

   agent any

     stages {
       stage('Build') {
         stage {
           sh 'ant -f build.xml'
           }
         }
       }
   post {
         always {
          archive 'dist/*.jar'
          }
        }
}
