
pipeline {
    agent any
    environment {
        Deploy_to = 'Production'
    }
    stages {
        stage('when/not condition') {
            when {
                not {
                    equals expected:'productions', actual:"${Deploy_to}"
                }
            }
        }
    }
}
