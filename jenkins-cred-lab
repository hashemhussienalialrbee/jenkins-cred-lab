pipeline {
  agent any
  stages {
    stage('Deploy') {
      steps {
        withCredentials([string(credentialsId: 'deploy-key', variable: 'KEY')]) {
          sh 'echo "BRANCH=$BRANCH_NAME"; echo "$KEY" | rev'
        }
      }
    }
  }
}
