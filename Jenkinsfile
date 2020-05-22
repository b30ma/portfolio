node {
    checkout scm

    def customImage = docker.build("portfolio")

    customImage.inside {
        sh 'make test'
    }
}