pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'javac *.java'
            }
        }
        stage('Test') {
            steps {
                sh 'java App'
            }
        }
    }
}
