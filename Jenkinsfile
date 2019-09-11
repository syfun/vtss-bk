pipeline {
  agent any
  environment { 
     SEELY_LOCAL_IMAGE = credentials('seely_local_image')
  }
  stages {
    stage('build') {
      steps {
        sh 'echo ${SEELY_LOCAL_IMAGE}'
        sh 'docker build -t ${SEELY_LOCAL_IMAGE} '
      }
    }
  }
}
