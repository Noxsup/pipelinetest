pipeline{
    agent any
    environment {
        // course = "gcp"
        Deploy_to = "productions"

    }
    stages {
        stage('when example') {
            when {
                environment name : 'Deploy_to', value: 'production'
            }
            steps {
                echo "deploying in jenkins"
            }
        }
    }
}
