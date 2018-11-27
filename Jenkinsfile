pipeline {
  
  agent any
  stages {
    stage('Information') {
      steps {
        bat 'node -v'
        bat 'npm -v'
      }
    }

    stage('Dependencies') {
      steps {
        bat 'npm install'
      }
    }

    stage('Build') {
      steps {
        bat 'npm run build'
      }
    }   
  }
}
