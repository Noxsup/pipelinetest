//allOf
pipeline {
    agent any 
    environment {
        DEPLOY_TO = "siva" // static , hard
    }
    stages {
        stage ('Example Build') {
            steps {
                echo "Build stage!!!!!!"
            }
        }
        stage ('Deploy') {
            when {
                allOf {
                    branch 'production'
                    environment name: 'DEPLOY_TO', value: 'siva'
                }
            }
            steps {
                echo "Deploying in Prod environment"
            }
        }
    }
}
