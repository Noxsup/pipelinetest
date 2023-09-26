pipeline {
    agent any
    environment {
        deploy_to = 'production'
    }
    stages {
        stage ('Example Build'){
            steps{
                echo 'Build Stage SHINEEEEEEEEEEEEEE'
            }
            
        }
        stage ('Deploy') {
            when {
                allof {
                    branch 'production'
                    environment name: 'deploy_to', value: 'siva'                
                }
                steps {
                    echo "Deploying in prod environment"
                }
            }
        }
    }
}
