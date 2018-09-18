pipeline {

   agent any

     stages {
       stage('build') {
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
