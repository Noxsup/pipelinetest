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
                anyOf {
                    expression {
                        BRANCH_NAME ==~ /(production|staging)/
                    }
                    environment name: 'DEPLOY_TO', value: 'siva'
                }
            }
            steps {
                echo "Deploying in nonprod environment"
            }
        }
        stage ('prod'){
            when {
                buildingTag()
            }
            steps {
                echo "Deploying to prod Kubernetes cluster"
            }
        }
    }
}
