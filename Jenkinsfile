pipeline {
    agent any
    environment {
        Deploy_to = 'productions'
    }
    stages {
        stage('When example / allof') {
            when {
                allof {
                    branch "production"
                    environment name: 'Deploy_2', value: 'production'
                }
            }
            steps {
                echo "All conditions are satisfied"
            }
        }
        stage('second stage'){
            steps {
                echo "Execute, bla la la la "
            }
        }
 }
}
