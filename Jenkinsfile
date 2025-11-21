pipeline {
    agent {
        label 'java-slave'
    }
    stages {
        stage ('Build') {
            steps {
                echo "Building the application"
            }
        }
        stage ('Scans') {
            steps {
                echo "Performing the scans"
            }
        }
        stage ('DeploytoDev') {
            steps {
                echo "***** Deploying to dev env ******"
            }
        }
        stage ('DeploytoTest') {
            steps {
                echo "***** Deploying to Test env ******"
            }
        }   
        stage ('DeploytoStage') {
            when {
                expression {
                    BRANCH_NAME ==~ /(production|staging)/
                }
            }
            steps {
                echo "***** Deploying to Stage env ******"
            }
        }
        stage ('DeploytoProd') {
            when {
                expression {
                    BRANCH_NAME ==~ /(production|staging)/
                }
            }
            steps {
                echo "***** Deploying to Prod env ******"
            }
        }
    }
}
