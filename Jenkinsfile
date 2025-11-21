pipeline {
    agent {
        label 'java-slave'
    }
    environment {
        DEPLOY_TO = 'production'
    }
    stages {
        stage('ProdEnv'){
            when {
                environment name: 'DEPLOY_TO', value: 'production'
            }
            steps {
                echo "***** Deploying to production"
            }
        }
    }
}
