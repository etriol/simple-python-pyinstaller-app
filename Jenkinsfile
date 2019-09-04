pipeline {
  agent {
    docker {
      image 'cdrx/pyinstaller-linux:python2'
    }

  }
  stages {
    stage('error') {
      steps {
        sh 'npm install'
      }
    }
    stage('delivery') {
      steps {
        sh 'pyinstaller --onefile sources/add2vals.py'
      }
    }
  }
}