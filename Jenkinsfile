pipeline {

    agent { label 'docker-agent' }

    stages {

        stage('Build Image') {
            steps {
                script {
                    def version = env.BUILD_NUMBER

                    sh """
                        echo BUILD_NUMBER=${version}
                        docker build -t app-ci-cd:${version} .
                        docker tag app-ci-cd:${version} app-ci-cd:latest
                        docker image ls | grep app-ci-cd
                    """
                }
            }
        }

    }
}
