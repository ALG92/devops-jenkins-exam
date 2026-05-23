pipeline {
    agent any

    stages {

        stage('Build Docker') {
            steps {
                sh '''
                export GIT_SSH_COMMAND="ssh -o StrictHostKeyChecking=no"
                docker-compose build
                '''
            }
        }

        stage('Run App') {
            steps {
                sh '''
                export GIT_SSH_COMMAND="ssh -o StrictHostKeyChecking=no"
                docker-compose up -d
                '''
            }
        }

    }
}
