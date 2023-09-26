pipeline {
    agent any
    stages {
        stage("When Example") {
            when {  
                expression {
                    BRANCH_NAME ==~ /(production|staging)/
                }
            }
            steps {
                echo "Deploying in Jenkins"
            }
        }
        stage ('SecondStage') {
            steps {
                echo "Execute , irrespsctive of the condition"
            }
        }
    }
}
