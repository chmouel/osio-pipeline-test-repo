def REPO = "https://github.com/chmouel/nodejs-health-check"

pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        library identifier: 'current@version', retriever: legacySCM(scm)
        script {
          osio {
            stages = ['run']
            repository = REPO
            application_remote_file = REPO.replace("https://github.com", "https://raw.githubusercontent.com") + "/master/.openshiftio/application.yaml"
            branch_name = "testing"
          }
        }
      }
    }
  }
}

// vim: ft=groovy
