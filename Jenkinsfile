pipeline {
    agent any
    stages {
        stage('hello AWS from Jenkins test') {
            steps {
                withAWS(credentials: 'aws-key') {
                    sh 'aws s3 ls'

                }
            }
        }
    }
}