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

    stage('Run test') {
      steps {
        sh 'docker run -itd --name proyapi --rm -p 5000:5000 rogermz/proyectoapi:1.1'
      }
    }

  }
}