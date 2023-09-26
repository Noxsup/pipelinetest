pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                echo 'Building maven application'
            }
        }
        stage("scan") {
            parallel {
                stage('Sonar') {
                    echo 'Performing sonar scans'
                    sleep 10
                }
                stage('Fortify') {
                    steps{
                        echo "Performing Fortify scans"
                        sleep 10 
                    }

                }
                 stage('Fortify') {
                    steps{
                        echo "Performing Fortify scans"
                        sleep 10 
                    }
                 }
            }

        }
        stage('Deploy'){
            steps {
                echo "Deploying to env"
            }

        }

    }
}
