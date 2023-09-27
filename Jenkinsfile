pipeline {
    agent any
    stages {
        stage ('Bulid') {
            steps {
                echo "Building" 
            }
        }
    }
    post {
        successs {
            echo "Post build ==> Success is called"
        }
        failure {
            echo "Post build ==> failure is called"
            // body, can be any code
            // mailer ===> SRE
        }
        always {
            echo "Post build ===> always is called"
        }
    }
}
