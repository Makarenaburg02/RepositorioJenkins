pipeline {
    agent {
        docker {
            image 'python:3.9-slim'
            args '-v /var/run/docker.sock:/var/run/docker.sock'  
        }
    }
    
    stages {
        stage('Build') {
            steps {
                echo 'Construyendo el proyecto...'
                sh 'python --version'
            }
        }
        
        stage('Security Scan') {
            steps {
                echo 'Instalando Bandit...'
                sh 'pip install bandit'
                
                echo 'Ejecutando análisis de seguridad...'
                sh 'bandit -r . || true'
            }
        }
    }
}