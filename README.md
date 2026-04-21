pipeline {
    agent any
    stages {
        stage('Build & Push') {
            steps {
                sh 'docker build -t <username>/app5:latest .'
                sh 'docker push <username>/app5:latest'
            }
        }
    }
}
