pipeline {
    agent { label 'docker' }

    stages {
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t app-ci-cd .'
            }
        }
    }
}


