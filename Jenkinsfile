pipeline {
    agent any 
    tools {
        maven 'Maven_3_5_0'
    }

    stages {
        stage('Compile stage') {
            steps {
                sh "mvn clean compile" 
        }
    }

         stage('testing stage') {
             steps {
                sh "mvn test"
        }
    }

          

  }

}