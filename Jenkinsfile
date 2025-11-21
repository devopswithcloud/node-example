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
                anyOf {
                  branch 'release-*'
                  tag pattern: "v\\d{1,2}.\\d{1,2}.\\d{1,2}", comparator: "REGEXP"
                }

            }
            steps {
                echo "***** Deploying to Stage env ******"
            }
        }
        stage ('DeploytoProd') {
            when {
                //v1.2.3
                tag pattern: "v\\d{1,2}.\\d{1,2}.\\d{1,2}", comparator: "REGEXP"
            }
            steps {
                echo "***** Deploying to Prod env ******"
            }
        }
    }
}
