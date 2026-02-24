pipeline {
    agent none

    stages {
        stage('Test Agent') {
            agent { label 'docker' }
            steps {
                sh 'echo NODE: $(hostname)'
                sh 'whoami'
                sh 'docker --version'
            }
        }
    }
}
