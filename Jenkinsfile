pipeline {
    agent any
    environment {
        DEPLOY_TO = 'production'
    }
    stages {
        stage("When Example") {
            when {  
                allOf {
                    branch 'production'
                    environment name: 'DEPLOY_TO', value: 'production'
                }
            }
            steps {
                echo "All conditions satisfied"
            }
        }
        stage ('SecondStage') {
            steps {
                echo "Execute , irrespsctive of the condition"
            }
        }
    }
}
