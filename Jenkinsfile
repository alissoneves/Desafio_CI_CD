pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/alissoneves/Desafio_CI_CD'
            }
        }
        stage('Build') {
            steps {
                echo 'Buildando projeto...'
            }
        }
        stage('Test') {
            steps {
                echo 'Rodando testes...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Fazendo deploy...'
            }
        }
    }
}
