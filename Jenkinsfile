pipeline {
  
  agent any
  tools {nodejs "node_11.3.0"}

  stages {
    stage('Informations') {
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
    
    stage ('push artifact') {
       steps {
         zip zipFile: 'artefacts/dist.zip', archive: false, dir: 'dist'
         archiveArtifacts artifacts: 'artefacts/*', fingerprint: true
       }
    }
    
    /*stage ('bat') {
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
    }*/
  }
}
