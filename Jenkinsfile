pipeline {
    agent any 
    tools {
        maven 'Maven 3.5.3'
        jdk 'jdk8'
    }
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
            }
        }
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
               sh 'mvn archetype:generate'
            }
        }
    }
}
