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
        sh 'cp index.cgi /srv/pythoncgi/index.cgi'
	sh 'chmod 755 /srv/pythoncgi/index.cgi'
      }
    }

  }
}
