pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    sh 'docker build -t app-ci-cd .'
                }
            }
        }

        stage('Run Container') {
            steps {
                script {
                    sh '''
                    docker stop app-container || true
                    docker rm app-container || true
                    docker run -d -p 3002:3000 --name app-container app-ci-cd
                    '''
                }
            }
        }
    }
}
