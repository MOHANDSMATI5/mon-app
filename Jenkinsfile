pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo '=== Recuperation du code ==='
                checkout scm
            }
        }

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

        bat '''
        echo Deploiement en cours...

        if not exist C:\\deploy\\mon-app mkdir C:\\deploy\\mon-app

        xcopy /E /Y /I * C:\\deploy\\mon-app

        echo Fichiers deployes ici :
        dir C:\\deploy\\mon-app
        '''
    }
}
    }

    post {
        always {
            echo 'Pipeline termine !'
        }
        success {
            echo 'SUCCESS: Deploiement OK 🚀'
        }
        failure {
            echo 'FAILURE: Erreur dans le pipeline ❌'
        }
    }
}
