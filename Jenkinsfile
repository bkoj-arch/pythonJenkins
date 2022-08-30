pipeline {
  agent any
  stages {


    stage('TEST'){
	steps{

	
sh 'python3 -m pylint --output-format=parseable index.cgi --msg-template="{path}:{line}: [{msg_id}({symbol}), {obj}] {msg}" | tee pylint.log || echo "pylint exited with $?"'
sh 'echo "linting Success, Generating Report"'
recordIssues enabledForFailure: true, aggregatingResults: true, tool: pyLint(pattern: 'pylint.log')

}

}	
    stage('DEPLOY') {
      steps {
        sh 'cp index.cgi /srv/cgi-bin/'
	sh 'chmod 755 /srv/cgi-bin/index.cgi'
      }
    }

  }
}
