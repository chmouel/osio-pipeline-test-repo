def TEST_YAML = "https://raw.githubusercontent.com/chmouel/nodejs-health-check/master/.openshiftio/application.yaml"
pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        library identifier: 'current@version', retriever: legacySCM(scm)
        script {
          osio {
            application_remote_file = TEST_YAML
          }
        }
      }
    }
  }
}

// vim: ft=groovy
