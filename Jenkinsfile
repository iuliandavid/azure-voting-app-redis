pipeline {
    agent any

    stages {
        stage('Verify branch') {
            steps {
                sh (script: "$GIT_BRANCH")
            }
        }
    }
}