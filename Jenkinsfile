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

   /* stage('Dependencies') {
      steps {
        bat 'npm install'
      }
   }

    stage('Build') {
      steps {
        bat 'npm run build'
      }
    } 
    
    stage ('push artifact') {
       steps {
         zip zipFile: 'artefacts/dist.zip', archive: false, dir: 'dist'
         archiveArtifacts artifacts: 'artefacts/*', fingerprint: true
       }
    }*/
    
    stage ('Deploy artifact') {
       steps { 
         bat 'dir .'
         sh 'echo $PATH'
         ansiblePlaybook playbook: './gdvsv802playbook.yml'
       }
    }
  }
}
