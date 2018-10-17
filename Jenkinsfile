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
    stage('error') {
      agent {
        docker {
          image 'centos:7'
        }

      }
      steps {
        sh 'echo foo'
      }
    }
    stage('wat') {
      steps {
        milestone(ordinal: 1, label: 'ohai')
      }
    }
  }
}