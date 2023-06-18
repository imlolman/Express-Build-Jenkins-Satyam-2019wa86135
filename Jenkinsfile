pipeline {
    agent any

    stages {
        stage('Install') {
            steps {
                sh 'npm install'
            }
        }
        stage('Package') {
            steps {
                sh 'node compress.js'
            }
        }
    }
    post {
        always {
            archiveArtifacts artifacts: 'build.zip', fingerprint: true
        }
    }
}

