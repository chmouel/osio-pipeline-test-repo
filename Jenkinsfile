pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        library identifier: 'current@version', retriever: legacySCM(scm)
        osio {
          application_remote_file: "https://raw.githubusercontent.com/chmouel/nodejs-health-check/master/.openshiftio/application.yaml"
        }
      }
    }
  }
}

// vim: ft=groovy
