pipeline {
    agent any 
    stages {
        stage ('Clone repository') {
            checkout scm 
        }
        stage('Build') {
            steps {
               echo "Hello this is jenkins pipeline"
            }
        }
    }
}
