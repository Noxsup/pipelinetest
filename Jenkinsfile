pipeline {
    agent any
    stages {
        stage('Branch example'){
            when {
                expression {
                    Branch_name ==~ /{production|staging}/
                }
            }
            steps {
                echo "Deploying in Jenkins "
            }
        }
        stage('Second stage') {
            steps {
                echo "Execute, irrespective of the conditions"
            }
        }
    }
}
