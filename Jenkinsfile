pipeline {
agent any
stages {
    stage('S3download') {
      steps {
    withAWS(credentials:'aws-key') {
        s3Upload(file:'FE', bucket:'yasminsalon.com', path:'.')
      }
    }
    }
}
}