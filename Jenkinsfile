pipeline {
    agent any
    stages {
        stage('hello AWS from Jenkins') {
            steps {
                withAWS(credentials: 'id') {
                    sh 'aws s3 ls'

                }
            }
        }
    }
}