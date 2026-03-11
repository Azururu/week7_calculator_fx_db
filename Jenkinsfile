pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }
        stage('Build Docker Image') {
            steps {
                bat 'docker build -t azuruu/sum-product_fx .'
            }
        }
        stage('Run Docker Compose') {
            steps {
                bat 'docker-compose up -d'
            }
        }
    }
}