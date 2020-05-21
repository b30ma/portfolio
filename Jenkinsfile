pipeline {
    agent any 

    stages {
        stage('Compile Stage') { 

            steps {
                Maven(maven : 'maven_3_5_0') {
                     sh 'mvn clean compile'

                }
            }
        }
        
        stage('Testing Stage') { 

            steps {
                 Maven(maven : 'maven_3_5_0') {
                     sh 'mvn clean test'

                }
            }
        }

        stage('Deployment Stage') { 

            steps {
                Maven(maven : 'maven_3_5_0') {
                     sh 'mvn clean deploy'

                }
            }
        }       
    }    
}