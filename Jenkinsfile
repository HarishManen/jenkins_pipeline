pipeline {

   agent any

     stages {
       stage ('Build') {
         steps {
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
