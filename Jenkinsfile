pipeline {
     agent any
     stages {
         stage('Build B-Test Project') {
              steps {
                sh '''
                 pwd
                 cd backend/b-test/src/main/
                 /opt/apache-maven-3.6.3/bin/mvn clean install -DskipTests
                 '''
              }
         }
     }
}