pipeline {
    agent {
        docker {
            image 'python:3.9-alpine'
        }
    }

    stages {
        stage('Build') {
            steps {
                echo 'Construyendo el proyecto...'
                sh 'python --version'
            }
        }
        stage('Test') {
            steps {
                echo 'Ejecutando pruebas unitarias...'
                sh 'python -m unittest discover -v'
            }
        }
    }
}