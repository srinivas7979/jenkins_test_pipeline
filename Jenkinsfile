pipeline {
    agent any 
    stages {
        stage ('Clone repository') {
            steps {
            checkout scm
            }
        }
        stage('Build') {
            steps {
               echo "Hello this is jenkins pipeline"
               def mvn_version = '/opt/apache-maven-3.5.3'
               withEnv( ["PATH+MAVEN=${tool mvn_version}/bin"] )
               sh 'mvn -Dmaven.test.failure.ignore=true install'
            }
        }
    }
}
