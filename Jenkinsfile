pipeline {
    agent any 
    environment {
        deploy_to = 'Naruto'
    }
    stages {
        stage('build') {
            when {
                anyOf {
                    expression {
                        Branch_name ==~ /production|staging/
                    }
                    environment name: 'deploy_to', value: 'Sasuke'

                }
            }
            steps {
                echo "SHINEEEEEEEEEEEEEEEEEEEE"
            }
        }
    }
}
