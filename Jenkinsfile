pipeline {
	agent {
    node {
      label 'linux && nodejs'
    }
  }

  stages {
    stage('Build') { 
      steps {
        sh 'npm install' 
      }
    }
    stage('Test') {
      steps {
        sh './jenkins/scripts/test.sh'
      }
    }
  }
}
