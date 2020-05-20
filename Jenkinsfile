pipeline {
    agent any 

    stages {
        
        stage('Testing Stage') { 

            steps {
                 withMaven(maven : 'maven_3_5_0') {
                     sh 'mvn clean test'

                }
            }
        }

        stage('Deployment Stage') { 

            steps {
                 withMaven(maven : 'maven_3_5_0') {
                     sh 'mvn clean deploy'

                }
            }
        }       
    }    
}