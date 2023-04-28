pipeline {
	agent {
    node {
      label 'linux && nodejs'
    }
  }

  triggers {
    pollSCM('*/2 * * * *')
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
