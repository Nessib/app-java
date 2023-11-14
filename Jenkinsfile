pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'javac *.java'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh 'java App'
                }
            }
            post {
                failure {
                    emailext attachLog: true, 
                              body: 'Votre message personnalisé en cas d\'échec.',
                              subject: "Échec de la construction de ${currentBuild.fullDisplayName}", 
                              to: 'necibmakrem25@example.com'
                }
            }
        }
    }
}

