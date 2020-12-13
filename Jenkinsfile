pipeline {
agent any
stages {
    stage('S3download') {
      steps {
    withAWS(credentials:'aws-key') {
        s3Download(file: 'index.html', bucket: 'yasminsalon.com')
      }
    }
    }
}
}