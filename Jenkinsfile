pipeline {
agent any
stages {
    stage('S3download') {
      steps {
    withAWS(credentials:'aws-key') {
        s3Upload(file:'halab_infra', bucket:'yasminsalon.com', path:'/')
      }
    }
    }
}
}