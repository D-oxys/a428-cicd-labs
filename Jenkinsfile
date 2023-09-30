pipeline {
    agent any  // Menggunakan agen Jenkins yang tersedia

    environment {
        NODE_HOME = tool name: 'NodeJS', type: 'Tool'
    }

    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
    }

    post {
        success {
            echo 'Proyek berhasil dibangun dan diuji.'
        }
        failure {
            echo 'Proyek gagal dibangun atau diuji. Perlu tindakan lebih lanjut.'
        }
    }
}
