pipeline {
  agent none
  stages {
    stage('hello') {
      parallel {
        stage('hello') {
          steps {
            echo 'Hello World'
          }
        }
        stage('world') {
          steps {
            echo 'ohai'
          }
        }
      }
    }
  }
}