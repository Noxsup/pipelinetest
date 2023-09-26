
pipeline {
    agent any
    stages {
        stage('Whats happening') {
            when {
                expression {
                    Branch_name ==~ /{production|staging}/
                } 
            }
            steps {
                echo "deploying in jenkins"
            }
        }
        stage('Secondstage'){
            echo "Execute, irrespective of condition"
        }
    }
}
