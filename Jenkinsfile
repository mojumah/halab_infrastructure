pipeline {
    agent any
    stages {
        stage('hello AWS') {
            steps {
                withAWS(credentials: 'id') {
                    sh 'aws s3 ls'

                }
            }
        }
    }
}
