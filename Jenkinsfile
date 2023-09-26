pipeline {
    agent any 
    environment {
        deploy_to = 'siva' //static, hard
    }
    stages {
        stage('Build stage') {
            steps {
                echo "Build stage"
            }
        }
        stage ('Deploy') {
            when {
                anyOf {
                    expression {
                        Branch_name = 'production'
                    }
                }
                environment name: 'production', value: 'siva'
                
            }
            steps {
                echo 'Deploying in non prod '
            }
        }
        stage('prod') {
            when {
                //changeRequest() ===> PR's only
                //buildingTag()
                // buildingTag will execute when we are building a tag
                // tag will execute only when we are executign a specfic pattern
                //tag "release-*"
                //vx.x.x v1.2.3
                tag pattern: "v\\d{1,2}.\\d{1,2}.\\{1,2}", comparator: "REGEXP"
            }

        }

    }
}
