pipeline {
    agent {
        label 'java-slave'
    }

    environment {
        // key = value
        course = "Kubernetes"
        name = "Siva"
    }

    stages {
        stage('Build') {
            environment {
                cloud = "GCP"
            }
            steps {
                echo "**** Building the application *****"
                echo "**** Welcome ${name} *******"
                echo "**** You enrolled to ${course} , All the best ${name}*****"
            }
        }
        stage ('SecondStage'){
            steps {
                echo "**** Welcome ${name} *******"
                echo "*** You are certified in ${cloud} Cloud"
            }
        }
    }
}

// ${env.variable}
// ${params.varible}
