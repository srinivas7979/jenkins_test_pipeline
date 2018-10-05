pipeline {
    agent any 
    tools {
        maven 'MY_MVN'
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
        stage ('Clone repository') {
            steps {
            checkout scm
            }
        }
        stage('Build') {
            steps {
               echo "Hello this is jenkins pipeline"
               sh 'cd "${WORKSPACE}/1.0" && mvn -Dmaven.test.failure.ignore=true install' 
               
            }
        }
    }
}
