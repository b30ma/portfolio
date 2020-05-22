pipeline {
    agent {
        docker { image 'portfolio' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'node --version'
            }
        }
    }
}