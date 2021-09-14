pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'hello world'
        sh 'pwd'
        sh 'export'
        sh 'ls -latrh'
        sh '''echo $GIT_URL | awk -F\'/\' \'{ print $(NF) }\' | sed \'s/.git$//\'
'''
      }
    }

  }
}