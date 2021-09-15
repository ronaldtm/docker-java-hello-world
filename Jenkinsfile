pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'javac HelloWorld.java'
        sh 'docker build -t hello-world:8u131 -f Dockerfile-8u131 .'
      }
    }

    stage('run') {
      steps {
        sh 'docker run -it --rm=true hello-world:8u131'
      }
    }

  }
}