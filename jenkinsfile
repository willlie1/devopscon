pipeline {
   agent any
   tools {
      maven "M3"
   }
   stages {
      stage('Build') {
         steps {
            git 'https://github.com/willlie1/devopscon.git'
            sh "mvn clean install"
         }
         post {
            success {
               junit '**/target/surefire-reports/TEST-*.xml'
            }
         }
      }
   }
}
