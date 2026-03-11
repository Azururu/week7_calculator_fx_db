pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Azururu/week7_calculator_fx_db.git'
            }
        }
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