pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'hello world'
        sh 'pwd'
        sh 'export'
        sh 'ls -latrh'
        sh '''export APP_NAME=`echo $GIT_URL | awk -F\'/\' \'{ print $(NF) }\' | sed \'s/.git$//\'`
'''
      }
    }

    stage('error') {
      steps {
        echo '$APP_NAME'
        sh 'echo $APP_NAME'
      }
    }

  }
}