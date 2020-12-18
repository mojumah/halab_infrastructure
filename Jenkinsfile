@Library('github.com/releaseworks/jenkinslib') _

node {
  stage('S3Sync') {
      steps {
    withCredentials ([[$class: 'UsernamePasswordMultiBinding', credentialsId: 'aws-key', usernameVariable: 'AWS_ACCESS_KEY_ID', passwordVariable: 'AWS_SECRET_ACCESS_KEY']])
     {
        AWS("--region=eu-west-2 aws s3 sync . s3://yasminsalon.com")
     }
  }
}