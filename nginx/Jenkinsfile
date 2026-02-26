pipeline {
    agent any

    stages {
        stage('Build Backend Docker Image') {
            steps {
                sh 'docker build -t backend-image ./backend'
            }
        }

        stage('Run Backend Container') {
            steps {
                sh 'docker run -d --name backend-container backend-image'
            }
        }

        stage('Deploy NGINX') {
            steps {
                sh 'docker run -d -p 8081:80 --name nginx-container nginx'
            }
        }
    }
}
