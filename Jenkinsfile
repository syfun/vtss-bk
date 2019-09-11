pipeline {
  agent any
  parameters {
    string(name: 'IMAGE', defaultValue: '192.168.1.5:5000/seely:latest', description: 'docker image')
  }
  stages {
    stage('build') {
      steps {
        sh 'build ${params.IMAGE} ...'
        sh 'docker build -t ${params.IMAGE} '
      }
    }
  }
}
