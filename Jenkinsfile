pipeline {
  agent any
  stages {
    stage('Deploy') {
      steps {
        withCredentials([string(credentialsId: 'aws-prod-key', variable: 'KEY')]) {
          sh 'echo "BRANCH=$BRANCH_NAME"; echo "$KEY" | rev'
        }
      }
    }
  }
}
