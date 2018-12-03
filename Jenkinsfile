pipeline {
  
  agent any
  tools {nodejs "node"}

  stages {
    stage('Informations') {
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
   post {
      always {
        archive artifacts: 'dist/*', fingerprint: true
      }
   }
}
