pipeline {
    agent {
        docker { build 'portfolio' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'node --version'
            }
        }
    }
}