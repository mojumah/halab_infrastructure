@Library('github.com/releaseworks/jenkinslib') _

pipeline {
agent any
stages {
  stage("List S3 buckets") {
    steps {
    withCredentials([[$class: 'UsernamePasswordMultiBinding', credentialsId: 'aws-key', usernameVariable: 'AWS_ACCESS_KEY_ID', passwordVariable: 'AWS_SECRET_ACCESS_KEY']]) {
        AWS("--region=eu-west-1 s3 sync . s3://yasminsalon.com --exclude '.git/*'")
    }
    }
  }
}
}