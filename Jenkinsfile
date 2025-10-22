pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'git@github.com:Ikram-coder1/jenkins-pipeline-demo.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t jenkins-demo .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 8080:80 jenkins-demo || true'
            }
        }
    }
}
