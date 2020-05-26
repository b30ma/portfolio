node {
    def app

    stage('Clone repository') {
        /* Cloning the Repository to our Workspace */

        checkout scm
    }

    stage('Build image') {
        /* This builds the actual image */

        app = docker.build("simadock/portfolio")
    }

    stage('Run image') {
        

        docker.image("simadock/portfolio").withRun('-p 3306:3306') {
            /* do things */
        }
    }

    stage('Test image') {
        
        app.inside {
            echo "Tests passed"
        }
    }

    stage('Push image') {
        /* 
			You would need to first register with DockerHub before you can push images to your account
		*/
        docker.withRegistry('https://registry.hub.docker.com', 'docker-hub') {
            app.push("${env.BUILD_NUMBER}")
            app.push("1.0.0")
            } 
                echo "Trying to Push Docker Build to DockerHub"
    }
}