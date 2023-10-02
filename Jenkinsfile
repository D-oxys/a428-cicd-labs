pipeline {
    agent any  // Menggunakan agen Jenkins yang tersedia
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') { 
            steps {
                echo 'Build berhasil!'
            }
        }
    }
}
