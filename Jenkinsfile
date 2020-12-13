pipeline {
agent any
stages {
    stage('S3Sync') {
      steps {
          sh 'aws s3 ls'
          sh 'aws s3 sync . s3://yasminsalon.com'
      }
    }
    }
}