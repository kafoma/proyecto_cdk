pipeline {
  agent any
  stages {
    stage('Inicio') {
      steps {
        sh 'env'
        echo 'Inicializando'
      }
    }

    stage('Instalación') {
      steps {
        sh 'cat versionImage | xargs ./scripts/build.sh'
      }
    }

    stage('Compilacion') {
      steps {
        sh '''gcc programa.c -o mi_programa
./mi_programa'''
      }
    }

    stage('Limpieza') {
      steps {
        sh 'rm mi_programa'
      }
    }

  }
}