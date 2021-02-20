pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
        when {
                branch 'development' 
            }
	steps {
                sh './jenkins/scripts/deliver-for-development.sh'
            }
	}
    }
  
}
