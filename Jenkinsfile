pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo '=== Etape 1 : Build ==='
                bat 'type README.md'
            }
        }

        stage('Test') {
            steps {
                echo '=== Etape 2 : Test ==='
                bat 'echo Tests en cours (pas encore config Node)'
            }
        }

        stage('Deploy') {
            steps {
                echo '=== Etape 3 : Deploy ==='
                echo 'Application deployee avec succes !'
            }
        }
    }

    post {
        always {
            echo 'Pipeline termine !'
        }
    }
}