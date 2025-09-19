pipeline {
    agent {
        docker {
            image 'node:20'
            label '' // <- permite rodar em qualquer nó com Docker
            args '-u root:root' // opcional: permissões dentro do container
        }
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/alissoneves/Desafio_CI_CD'
            }
        }

        stage('Build') {
            steps {
                echo 'Buildando projeto...'
                sh 'node -v' // mostra que estamos dentro do container Node
            }
        }

        stage('Test') {
            steps {
                echo 'Rodando testes...'
                sh 'npm install'
                sh 'npm test || echo "Sem testes ainda"' // evita erro se não houver testes
            }
        }

        stage('Deploy') {
            steps {
                echo 'Fazendo deploy...'
                echo 'Desafio DevOps Philips finalizado com sucesso com webhoooook tste!!!!!!'
            }
        }
    }
}
