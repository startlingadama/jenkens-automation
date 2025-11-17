pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git url: 'https://github.com/startlingadama/jenkens-automation.git', branch: 'main'
            }
        }

        stage('Build Docker image') {
            steps {
                sh 'docker build -t python-app .'
            }
        }

        stage('Run image') {
            steps {
                sh 'docker run --rm python-app'
            }
        }
    }
}
