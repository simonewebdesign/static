pipeline {
  agent any
  stages {
    stage('Upload to AWS') {
      steps {
        withAWS(region:'eu-west-2',credentials:'aws-static') {
          sh 'echo "Hello World"'
          s3Upload(file:'index.html', bucket:'jenkins-static-bucket')
        }
      }
    }
  }
}
