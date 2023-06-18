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
                sh 'zip -r ../${BUILD_NUMBER}.zip *'
            }
        }
    }
}

