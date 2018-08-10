pipeline {
  agent any
  stages {
	stage('Test') {
      steps {
		library identifier: 'current@version', retriever: legacySCM(scm)
      }

	}
  }
}

// vim: ft=groovy
