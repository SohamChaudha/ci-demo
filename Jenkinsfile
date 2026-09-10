pipeline {
  agent any 
  stages {

    stage('Checkout') {
      steps {
      echo 'Checking out....'
      }
    }
    
    stage('Build') {
      steps {
      echo 'Building....'
      }
    }

    stage('Test') {
      steps {
      echo 'Testing....'
      }
    }

    stage('Deploy') {
      when {
       branch 'main' 
      }
      echo 'Deploying....' 
    }
  }

  post {
    always {
      archiveArtifacts artifacts: 'test-reports/**', allowEmptyArchive: true
    }

    success {
      echo 'Pipeline completed successfully'
    }

    faliure {
      echo 'Pipeline Failed'
    }
    
  }
  
}
