pipeline {
  agent any
  stages {
    stage('Upload to AWS') {
      steps {
        withAWS(credentials:'AKIA4DTVEONP6AIGRWJO') {
          s3Upload(file:'index.html', bucket:'jenkins-static-bucket', path:'index.html')
        }
      }
    }
  }
}
