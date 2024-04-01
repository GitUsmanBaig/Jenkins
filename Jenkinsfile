stage('Checkout') {
    steps {
        git 'https://github.com/GitUsmanBaig/Jenkins'
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

stage('Test') {
    steps {
        script {
            sh 'npm test'
        }
    }
}


