pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/dr-programmer/jenkins-demo.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                echo 'No build step for this simple app.'
            }
        }

        stage('Deploy') {
            steps {
                sh 'npm install pm2 -g || true'
                sh 'pm2 start index.js || pm2 restart index.js'
            }
        }
    }
}
