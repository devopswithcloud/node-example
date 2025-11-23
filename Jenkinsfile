pipeline {
    agent {
        label 'java-slave'
    }

    stages {
        stage('DockerBuild'){
            steps {
                echo "**************** Building the docker image ****************"
                sh "docker build -t i27devopsb8/node:v7 ."
                echo "*************** Listing the docker images ****************"
                sh "docker images"
            }
        }
    }
}

