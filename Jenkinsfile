pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        // Install Firebase Tools
        sh 'npm install -g firebase-tools'
      }
    }
    stage('Testing') {
      steps {
        // Deploy to Firebase Testing
        sh 'firebase deploy --only hosting:testing'
      }
    }
    stage('Staging') {
      steps {
        // Deploy to Firebase Staging
        sh 'firebase deploy --only hosting:staging'
      }
    }
    stage('Production') {
      steps {
        // Deploy to Firebase Production
        sh 'firebase deploy --only hosting:production'
      }
    }
  }
}
