pipeline {
    agent {
        kubernetes {
            label "hoangguruu-default-agent"
            defaultContainer 'dind'
        }
    }

    stages{
        stage("Build and Push to ACR") {
            steps {
                sh "docker ps"
                sh "docker build --network=host -t myapp ."
                sh "docker ps"
            }
        }
    }
}