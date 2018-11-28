pipeline {
  
  agent any
  stages {
    stage('Informations') {
      steps {
        node -v
        bat 'npm -v'
      }
    }

    stage('Dependencies') {
      steps {
        bat 'npm install'
      }
    }

    stage('Test') {
      steps {
        bat 'npm run lint'
      }
    }


    stage('Build') {
      steps {
        bat 'npm run build'
      }
    }   
  }
}
