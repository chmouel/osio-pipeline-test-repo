pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        library identifier: 'current@version', retriever: legacySCM(scm)
        osio {

        }
      }
    }
  }
}

// vim: ft=groovy
