pipeline {
    agent any
    stages {
        stage('hello AWS') {
            steps {
                withAWS(credentials: 'id', credentials: 'secret') {
                    sh 'aws s3 ls'

                }
            }
        }
    }
}