pipeline {
    agent any

    stages {
       stage('Checkout') {
    steps {
        sh '''
        if [ ! -d "Jenkins" ]; then
            git clone https://github.com/GitUsmanBaig/Jenkins.git
        else
            echo "Directory already exists, skipping clone."
        fi
        '''
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
                    echo 'npm run build'
                }
            }
        }

        // Stage 4: Run tests
        stage('Test') {
            steps {
                script {
                    echo 'npm run test'
                }
            }
        }

        // Stage 5: Dockerization and Deployment
        stage('Dockerize and Deploy') {
            steps {
                script {
                    sh 'sleep 2m'
                    sh 'echo docker-compose up -d'
                }
            }
        }
    }
}
