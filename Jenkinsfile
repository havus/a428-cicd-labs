pipeline {
	agent {
    node {
      label 'linux && nodejs'
    }
  }

  triggers {
    pollSCM('H/2 * * * *')
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
