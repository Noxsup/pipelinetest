pipeline {
    agent any
    environment {
        Deploy_to ='Poductionss'
    }
    stages {
        stage('When Example') {
            when {
                not {
                    equals expected: 'Producns', actual: '${Deploy_to}'
                }
            }
            steps {
                echo "Deploy in Jenkins"
            }
        }
    }
}
