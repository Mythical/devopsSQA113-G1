pipeline {
    agent any
    
    environment {
        FIREBASE_TOKEN = credentials('firebase-token')  // Ensure this matches the environment variable you added in Jenkins
    }
    
    stages {
        stage('Checkout SCM') {
            steps {
                checkout scm
            }
        }
        
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Deploy to Firebase') {
            steps {
                sh 'firebase deploy --token $FIREBASE_TOKEN'
            }
        }
    }
}

