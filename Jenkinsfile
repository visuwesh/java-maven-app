pipeline {
  agent any
  stages {
    stage ('Build') {
        sh 'echo test'
        sh '''
            echo "multi line"
            ls -lrt
        '''
    }
  }
}
