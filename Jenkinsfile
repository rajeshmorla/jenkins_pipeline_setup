pipeline {
  agent any
  stages {
    stage('Git Pull') {
      steps {
        git(url: 'https://github.com/rajeshmorla/jenkins_pipeline_setup.git', branch: 'master')
      }
    }

    stage('Is Run Required ?') {
      parallel {
        stage('Is Run Required ?') {
          steps {
            echo 'Checking condition'
            readFile 'Build.json'
            writeFile(file: 'QA', text: 'hello')
            waitUntil(initialRecurrencePeriod: 3) {
              echo 'hello'
            }

          }
        }

        stage('hiii') {
          steps {
            echo 'hiii'
          }
        }

      }
    }

  }
}