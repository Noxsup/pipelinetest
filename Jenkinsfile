pipeline {
	agent any
	environment {
		course = 'Devops Mastery'
		name = 'SK'
	}
	stages {
		stage('build') {
			environment {
				git_creds = credentials('GitCredwithToken') // id for credentials
			}
			steps {
				echo "Git creds are ${git_creds}"
				echo "userid is ${git_creds_USR}"
				echo "passwordd is ${git_creds_PSW}"
			}
			
		}
	}
}
