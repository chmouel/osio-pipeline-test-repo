def TEST_YAML = "https://raw.githubusercontent.com/chmouel/nodejs-health-check/master/.openshiftio/application.yaml"
pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        library identifier: 'current@version', retriever: legacySCM(scm)
        script {
          sh "mkdir -p .openshiftio && curl -o .openshiftio/application.yaml ${TEST_YAML}"
          osio {
            stages = ['run', 'stage']
          }
        }
      }
    }
  }
}

// vim: ft=groovy
