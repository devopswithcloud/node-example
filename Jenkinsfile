pipeline {
    agent {
        label 'java-slave'
    }
    tools {
        maven 'MAVEN_3.8.8' // the same name should be configured in the tools section
    }
    stages {
        stage ("Maven") {
            steps {
                echo "hello, this is maven section"
                sh "mvn --version"
            }
        }
        stage ("SecondStage") {
            // what ever u write under the stage will be taking presedence
            tools {
                maven 'MAVEN_3.9.6' 
            }
            steps {
                echo "hello from second stage"
                sh "mvn --version"
            }
        }
    }
}
