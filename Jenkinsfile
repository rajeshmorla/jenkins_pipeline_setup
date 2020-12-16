pipeline {
  agent any
  stages {
    stage('Git Pull') {
      steps {
        git(url: 'https://github.com/rajeshmorla/jenkins_pipeline_setup.git', branch: 'master')
      }
    }

    stage('Is Run Required ?') {
      steps {
        echo 'Checking condition'
        readFile 'Build.json'
        writeFile(file: 'QA', text: 'hello')
      }
    }

  }
}