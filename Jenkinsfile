pipeline {
    agent any
    environment {
        Deploy_to ='Productions'
    }
    stages {
        stage('When Example') {
            when {
                not {
                    equals expected: "productions", actual: "${Deploy_to}"
                }
            }
            steps {
                echo "Deploy in Jenkins"
            }
        }
    }
}
