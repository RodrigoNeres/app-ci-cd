stage('Build Image') {
    steps {
        script {

            def version = "${env.BUILD_NUMBER}"

            sh """
                echo ===== DEBUG =====
                echo BUILD_NUMBER=${env.BUILD_NUMBER}
                echo VERSION=${version}
                echo =================

                docker build -t app-ci-cd:${version} .
                docker tag app-ci-cd:${version} app-ci-cd:latest

                docker image ls | grep app-ci-cd
            """
        }
    }
}
