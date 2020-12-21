pipeline {
  agent any
  stages {
    stage('Git Pull') {
      steps {
        git(url: 'https://github.com/rajeshmorla/jenkins_pipeline_setup.git', branch: 'master')
      }
    }

    stage('Is Run Required ?') {
      when {
        expression {
          params.RUN_REQUIRED
        }

      }
      steps {
        echo 'Run is required, further stages should execute!'
      }
    }

  }
  parameters {
    booleanParam(name: 'RUN_REQUIRED', defaultValue: false)
    booleanParam(name: 'STATIC_CHECK', defaultValue: true)
    booleanParam(name: 'QA', defaultValue: true)
    booleanParam(name: 'UNIT_TEST', defaultValue: true)
    string(name: 'SUCCESS_EMAIL', defaultValue: 'rajeshmorla@live.com')
    string(name: 'FAILURE_EMAIL', defaultValue: 'rajeshmorla@live.com')
  }
}