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
               sh 'mkdir /tmp/hello'
               sh 'mvn install'
            }
        }
    }
}
