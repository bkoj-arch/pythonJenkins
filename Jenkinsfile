pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        sh 'echo Test'
      }
    }

    stage('DEPLOY') {
      steps {
        sh 'cp index.cgi /var/lib/jenkins/index.cgi'
	sh 'chmod 755 /var/lib/jenkins/index.cgi'
      }
    }

  }
}
