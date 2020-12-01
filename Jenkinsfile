pipeline {
  agent any
  stages {
    stage('Inicio') {
      steps {
        sh '''env
docker -v'''
        echo 'Inicializando'
      }
    }

    stage('Instalación') {
      steps {
        sh 'cat versionImage | xargs ./scripts/build.sh'
      }
    }

  }
}