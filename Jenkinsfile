pipeline {
  agent any
  parameters {
    string(name: 'IMAGE', defaultValue: '192.168.1.5:5000/seely:latest', description: 'docker image')
  }
  stages {
    stage('build') {
      when { branch 'master'}
      steps {
        sh "docker build -t ${params.IMAGE} ."
      }
    }
    stage('push') {
      when { branch 'master'}
      steps {
        sh "docker push ${params.IMAGE}"
      }
    }
  }
}
