pipeline {
  agent any
  stages {
    stage('build') {
      parallel {
        stage('build') {
          steps {
            sh 'echo "hello build"'
          }
        }

        stage('build2') {
          steps {
            sh 'echo "build2"'
          }
        }

      }
    }

    stage('testing') {
      steps {
        sh 'echo "testing was ok!"'
      }
    }

    stage('deploy') {
      steps {
        sh 'ech "rsync the build to servers"'
      }
    }

  }
}