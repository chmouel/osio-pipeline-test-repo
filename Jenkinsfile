pipeline {
  agent any
  stages {
	stage('Test') {
      steps {
		library identifier: 'current', retriever: legacySCM(scm)
      }

	}
  }
}

// vim: ft=groovy
