pipeline {
   agent any
   tools {
     maven 'M3'
   }
   stages {
      stage('checkout scm') {
         steps{
            git 'https://github.com/raju30devops/maven-total-flow.git'
         }
       }
      stage('Build') {
         steps{
           sh 'mvn clean complie'
         }
       }
      stage('Test') {
         steps {
           sh 'mvn test'
           junit '**/target/surefire-reports/TEST-*.xml'
         }
       }
      stage('Package') {
         steps {
           sh 'mvn package'
          }
       }
     }
}
