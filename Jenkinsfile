pipeline {
    agent any
    environment {
        deploy_to = 'Production'
    }
    stages {
        stage('Example of allOf') {
            steps {
                echo "Build stage, SHINEEEEEEEEEEEEEEEEE !!!!!!!!!!!!"
            }
        }
        stage ('Deploy') {
            when {
                allOf {
                    branch 'production'
                    environment name: 'deploy_to', value: 'Production'
                }
                steps {
                    echo "Deploying in Prod Environment"
                }
            }
        }
    }
}
