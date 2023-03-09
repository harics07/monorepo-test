pipeline {
     agent any
     stages {
         stage('Build B-Test Project') {
              steps {
                sh '''
                 pwd
                 cd backend/b-test/src/main/
                 /opt/apache-maven-3.6.3/bin/mvn clean install -DskipTests
                 cp target/a-test-0.1.0.jar /opt/projects/
                 '''
              }
         }
        stage('Build A-Test Project') {
            steps{
                sh '''
                 pwd
                 cd backend/a-test/src/main/
                 /opt/apache-maven-3.6.3/bin/mvn clean install -DskipTests
                 '''
            }
        }
        stage('Build C-Test Project') {
            steps{
                sh '''
                 pwd
                 cd backend/c-test/src/main/
                 /opt/apache-maven-3.6.3/bin/mvn clean install -DskipTests
                 '''
            }
        }
     }
}
