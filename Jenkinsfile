pipeline {
  
  agent any
  stages {
    stage('Information') {
      steps {
        sh 'node -v'
        sh 'npm -v'
      }
    }

    stage('Dependencies') {
      steps {
        sh 'npm install'
      }
    }

    stage('Build') {
      steps {
        sh 'npm run build'
      }
    }   
  }
}
