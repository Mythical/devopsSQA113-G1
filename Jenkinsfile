pipeline {
    agent any
    
    environment {
        FIREBASE_TOKEN = '1//06TpzRf1GxF6kCgYIARAAGAYSNwF-L9Ir5fW1VqTM2fHNFL3rqAGVSukiM_lzEOh_O7LUEBhpbNe41t4HoOwlOHVNcZ0SNf0rHKo'
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

