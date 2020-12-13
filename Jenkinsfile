pipeline {
agent any
stages {
    stage('S3Upload') {
      steps {
    withAWS(credentials:'aws-key') {
        s3Upload(bucket:'yasminsalon.com', includePathPattern:'**/*')
      }
    }
    }
}
}