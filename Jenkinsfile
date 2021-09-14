pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'hello world'
        sh 'pwd'
        sh 'export'
        sh 'ls -latrh'
        sh '''APP_NAME=`echo $GIT_URL | awk -F\'/\' \'{ print $(NF) }\' | sed \'s/.git$//\'`

docker run \\
  -v /var/run/docker.sock:/var/run/docker.sock \\
  -v $PWD:/workspace -w /workspace \\
  buildpacksio/pack build \\
    $APP_NAME \\
    --builder paketobuildpacks/builder:base

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