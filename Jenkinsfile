pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'Pipeline Status: Started'
        echo 'Build Status: Started'
        sh 'npm install'
        echo 'Build Status: Successful'
      }
    }

    stage('test') {
      steps {
        echo 'Test Status: Started'
        sh 'npm test'
        echo 'Test Status: Successful'
      }
    }

    stage('package') {
      steps {
        echo 'Package Status: Started'
        sh 'npm run package'
        echo 'Package Status: Successful'
      }
    }

    stage('archive') {
      steps {
        echo 'Extracting Artifact'
        archiveArtifacts '**/distribution/*.zip'
        echo 'Extracted Artifact'
      }
    }

  }
  tools {
    nodejs 'nodejs'
  }
  post {
    always {
      echo 'Pipeline Status: Completed'
    }

  }
}