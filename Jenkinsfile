pipeline {
    agent any

    stages {
        stage('Verify branch') {
            steps {
                sh "echo $GIT_BRANCH"
            }
        }

        stage('Docker build') {
            steps {
                sh "docker images -a"
                sh(script: """
                    cd azure-vote/
                    docker build -t jenkins-pipeline .
                    docker images -a
                    cd ..
                """)
            }
        }
    }
}