pipeline {

   agent any

     stages {
       stage ('unit Test') {
         steps {
           sh 'ant -f test.xml'
           }
         }
       stage ('Build') {
         steps {
           sh 'ant -f build.xml'
          }
       }
 stage('deploy') {

      steps {

      sh "cp dist/rectangle_${env.BUILD_NUMBER}.jar /var/www/html/rectangle/all/"
    }
   post {
         always {
          archiveArtifacts artifacts: 'dist/*.jar', fingerprint: true
          }
        }
}
