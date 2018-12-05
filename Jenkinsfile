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
    
    stage ('bat') {
       steps { 
         bat 'diru .'
       }
    }
    stage ('SH') {
       steps { 
         sh 'echo $PATH'
       }
    }
    stage ('deploy artefact'){
      steps { 
        ansiblePlaybook playbook: './gdvsv802playbook.yml'
       }
    }
  }
}
