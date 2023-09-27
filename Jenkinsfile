pipeline {
    agent any
    stages {
        stage ('Build') {
            steps {
                echo "Building!!!!"
                error {"Build failed"}
            }
        }
    }
    post {
        success {
            echo "Post build ===> Success is called "
        }
        failure {
            echo "Post build ===> Failure is called "
            // body, can be any code 
            // mailer ===> SRE 
        }
        always {
            echo "Post build ===> Always is called "

            // mail method ()
        }
    }
}
