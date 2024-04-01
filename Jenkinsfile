pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                sh 'git clone https://github.com/GitUsmanBaig/Jenkins.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                script {
                    sh 'npm install'
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    sh 'npm run build'
                }
            }
        }

        // Stage 4: Run tests
        stage('Test') {
            steps {
                script {
                    sh 'npm run test'
                }
            }
        }

        // Stage 5: Dockerization and Deployment
        stage('Dockerize and Deploy') {
            steps {
                script {
                    sh 'docker-compose up -d'
                }
            }
        }
    }
}
