pipeline {
  agent any
  stages {
    stage('Lint HTML') {
      steps {
        sh 'tidy -q -e *.html'
      }
    }
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
