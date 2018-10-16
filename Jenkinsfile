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
    stage('foo') {
      steps {
        echo 'foo'
      }
    }
    stage('') {
      agent {
        docker {
          image 'centos:7'
        }

      }
      steps {
        sh 'echo foo'
      }
    }
  }
}