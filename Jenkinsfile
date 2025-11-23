pipeline {
    agent {
        label 'java-slave'
    }
    environment {
        DOCKER_CREDS  = credentials('i27devopsb8_dockerhub_creds')
    }

    stages {
        stage('DockerBuild'){
            steps {
                echo "**************** Building the docker image ****************"
                sh "docker build -t i27devopsb8/node:v7 ."
                echo "*************** Listing the docker images ****************"
                sh "docker images"
                echo "*************** Docker login ****************************"
                sh "docker login -u ${DOCKER_CREDS_USR} -p ${DOCKER_CREDS_PSW}"
                sh "docker push i27devopsb8/node:v7"
            }
        }
    }
}

