pipeline {
	agent any
	environment {
		course = "Devops Mastery"
		name = "SK"
	}
	stages{
		stage('build'){
			environment {
				cloud = "GCP"
			}
			steps {
				echo "Welcome ${name}"
				echo "You enrolled for ${course} course"
				echo "you are certified in ${cloud} Course"
			}
		}
		stage('second stage'){
			steps {
				echo "Welcome ${name}"
				echo "You enrolled for ${course} course"
				echo "you are certified in ${cloud} Course"
			}
		}
	}
}
